<script setup>
defineProps({
  msg: String,
});
</script>

<template>
  <h1>{{ msg }}</h1>
  <p>This is my Snack Gallery to represent how much I eat. And to convince myself to eat healthier.</p>

  <div class="row">
    <div class="column">
      <p>Sour Patch Kids are bomb</p>
      <img src="../assets/sourpatch.webp" alt="Sour Patch Kids" />
    </div> 
    <div class="column">
      <p>Doritos Dinamitas are bomb</p>
      <img src="../assets/dinamitas.webp" alt="Doritos Dinamitas" />
    </div>
  </div>

  <div class="row">
    <div class="column">
      <p>Cheez-Its are bomb</p>
      <img src="../assets/cheezit.jpg" alt="Cheez-Its" />
    </div> 
    <div class="column">
      <p>Goldfish (Cheddar) are bomb</p>
      <img src="../assets/goldfish.jpg" alt="Goldfish" />
    </div>
  </div>

</template>

<style scoped>
img {
  display: block;
  margin: 0 auto;
  width: 300px;
  height: auto;
}

.column {
  float: left;
  width: 33.33%;
  padding: 50px;
}

.row::after {
  content: "";
  clear: both;
  display: table;
}
</style>
