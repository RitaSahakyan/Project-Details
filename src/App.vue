<template>
  <div id="app">
    <AppHeader />
    <HeaderComponent />
    <DescriptionComponent />
    <GalleryComponent />
    <AppFooter />
  </div>
</template>

<script>
import AppHeader from './components/AppHeader.vue';
import HeaderComponent from './components/HeaderComponent.vue';
import DescriptionComponent from './components/DescriptionComponent.vue';
import GalleryComponent from './components/GalleryComponent.vue';
import AppFooter from './components/AppFooter.vue';

export default {
  name: 'App',
  components: {
    AppHeader,
    HeaderComponent,
    DescriptionComponent,
    GalleryComponent,
    AppFooter
  }
}
</script>

<style>
* {
    margin: 0;
    padding: 0;
    text-decoration: none;
}
body{
    background-color: #ffffff;
    font-family: "DM Serif Display", serif;
}
ul, li{
    list-style-type: none;
}

.box-content{
    overflow: hidden;
}
  .container {
    padding-left: calc(50% - 1200px / 2);
    padding-right: calc(50% - 1200px / 2);
}
</style>
