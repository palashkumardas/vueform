<script setup>
import{ref,reactive} from 'vue';
const colorName= ref("None");

function getColor(){
  return {
    backgroundColor: colorName.value,
  }
}
</script>

<template>
    <section class="mx-auto container">
    <h1 class="text-2xl mb-10">Vue Form</h1>
    <p class="pb-5">Your Favorite Color:{{ colorName }}</p>
    <div>
      Your Favorite Color: 
      <input class="p-5" v-model="colorName" />
      <div class="w-32 h-32 mt-10" :style="getColor()"></div>
    </div>
  </section>
</template>

<style scoped>

</style>
