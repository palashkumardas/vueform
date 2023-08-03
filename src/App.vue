<script setup>
import{ref,reactive} from 'vue';

const person =reactive({
  name:'Palash',
  subject:'cse',
  age:30,
  job:'software engineer'
})
</script>

<template>
  <section class="mx-auto container">
    <h1 class="text-2xl mb-10">Vue Form</h1>
    <p class="mb-10">
      {{ person }}
    </p>
    
    <!-- <div class="flex flex-col mb-5 text-left" >
      <label for="name">Name</label>
      <input type="text" class="border border-gray-300 rounded-md p-2" v-model="person.name" />
    </div> -->

    <div class="flex flex-col mb-5 text-left" v-for="(value,key,index) in person" :key="index">
      <label for="name">{{ key }}</label>
      <input type="text" class="border border-gray-300 rounded-md p-2" v-model="person[key]" />
    </div>

  </section>
</template>

<style scoped>

</style>
