<template>
  <div class="gallery container">
    <img :src="$store.state.selectedImage" class="main-image" alt="Main Image" />
    <div class="thumbnails">
      <img 
        v-for="(image, index) in $store.state.images" 
        :key="index" 
        :src="image" 
        @click="$store.dispatch('updateSelectedImage', image)" 
        class="thumbnail" 
        :class="{ active: $store.state.selectedImage === image }"
        alt="Thumbnail"
      />
    </div>
  </div>
</template>
  
  <script>
  export default {
    name: 'GalleryComponent'
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