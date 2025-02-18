<script setup>
import { ref } from 'vue'

defineProps({
  msg: String,
})

const eggCount = ref(0)
const donutCount = ref(0)
const milkCount = ref(0)
</script>

<template>
  <h1>{{ msg }}</h1>

  <div>
    <p>Eggs: {{ eggCount }}</p>
    <button type="button" @click="eggCount++">+</button>
    <button type="button" @click="eggCount--">-</button>
  </div>

  <div>
    <p>Donuts: {{ donutCount }}</p>
    <button type="button" @click="donutCount++">+</button>
    <button type="button" @click="donutCount--">-</button>
  </div>

  <div>
    <p>Milk: {{ milkCount }}</p>
    <button type="button" @click="milkCount++">+</button>
    <button type="button" @click="milkCount--">-</button>
  </div>

</template>

<style scoped>
.read-the-docs {
  color: #888;
}
</style>
