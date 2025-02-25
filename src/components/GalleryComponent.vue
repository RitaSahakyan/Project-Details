<template>
    <div class="gallery container">
      <img :src="selectedImage" class="main-image" alt="Main Image" />
      <div class="thumbnails">
        <img 
          v-for="(image, index) in images" 
          :key="index" 
          :src="image" 
          @click="selectedImage = image" 
          class="thumbnail" 
          :class="{ active: selectedImage === image }"
          alt="Thumbnail"
        />
      </div>
    </div>
  </template>
  
  <script>
  export default {
    name: 'GalleryComponent',
    data() {
      return {
        images: [
          require('@/assets/min1.jpg'),
          require('@/assets/min2.png'),
          require('@/assets/min3.png')
        ],
                selectedImage: require('@/assets/min1.jpg')
      };
    }
  };
  </script>

  <style>
  .gallery{
    display: flex;
    flex-direction: column;
    align-items: center;
    height: 800px;
    margin-bottom: 44px;
  }
  .main-image {
    width: 1200px;
    min-height: 700px;
    max-height: 700px;
    border-radius: 30px;
    margin-bottom: 30px;
  }

  .thumbnails {
    display: flex;
    gap: 20px;
  }
  .thumbnail {
    width: 100px;
    height: 70px;
    border-radius: 5px;
    cursor: pointer;
    opacity: 0.7;
    transition: opacity 0.3s;
  }
  .thumbnail:hover, .thumbnail.active {
    opacity: 1;
  }
</style>