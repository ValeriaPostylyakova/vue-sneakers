<script setup>
import { onMounted, ref } from 'vue';

import axios from 'axios';
import Header from './components/Header.vue';
import List from './components/List.vue';
import Drawer from './components/Drawer.vue';

const items = ref([]); 

onMounted(async() => {
  try {
   const { data } = await axios.get('https://9b3fa2fbda761ff0.mokky.dev/items');
   items.value = data;
  } catch(array) {
    console.log(array);
  }
});
</script>

<template>
  <!-- <Drawer/> -->
  <div class="bg-white w-4/5 m-auto rounded-xl shadow-xl mt-14">
    <Header/>
    <div class="p-10">
      <div class="flex justify-between items-center">
        <h2 class="text-3xl font-bold mb-8">Все кроссовки</h2>
        <select class="py-2 px-3 border rounded-md outline-none">
          <option>По названию</option>
          <option>По цене (сначала дешёвые)</option>
          <option>По цене (сначала дорогие)</option>
        </select>
        <div class="relative flex items-center">
          <img class="absolute left-3" src="/search.svg" alt="">
          <input type="text" placeholder="Поиск..." class=" border rounded-md py-2 pl-10 pr-4 outline-none focus:border-gray-400">
        </div>
      </div>
      <div class="mt-10">
        <List :items="items"/>
      </div>
  </div>
</div>
</template>

<style scoped>

</style>