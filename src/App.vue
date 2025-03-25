<script setup>
import Grocery from './components/GroceryList.vue'
import GalleryPhotos from './components/Gallery.vue'
import Transitions from './components/Transitions.vue';
</script>

<template>
  <Grocery v-if="false" msg="Grocery List" />
  <GalleryPhotos v-if="false" msg="Snack Gallery"/>
  <Transitions/>
</template>

<style scoped>
</style>
