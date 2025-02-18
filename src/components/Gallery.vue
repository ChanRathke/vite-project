<script>
export default {

}
defineProps({
  msg: String,
})
</script>

<template>
  <h1>{{ msg }}</h1>

  <div>
    <p>Sour Patch Kids are bomb</p>
    <img :src="require('./assets/sourpatch.webp')"/>
  </div>

</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
