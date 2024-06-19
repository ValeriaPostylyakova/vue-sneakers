<script setup>
  defineProps({
    imageUrl: String,
    title: String,
    price: Number,
    isLike: Boolean,
    isAdded: Boolean,
    onClickLike: Function,
    onClickAdd: Function
  });
</script>

<template>
  <div class="relative bg-white border border-slate-100 transition rounded-3xl p-8 cursor-pointer hover:-translate-y-2 hover:shadow-xl">
    <img @click="onClickLike" :src="!isLike ? '/like-1.svg' :  '/like-2.svg'" alt="like" class="absolute top-8 left-8">
    <img :src="imageUrl" alt="sneaker">
    <p class="mt-2">{{ title }}</p>

    <div class="flex justify-between mt-5">
      <div class="flex flex-col">
        <span class="text-slate-400">Цена:</span>
        <span><b>{{ price }}руб.</b></span>
      </div>

      <img @click="onClickAdd" :src="!isAdded ? '/plus.svg' : './checked.svg'" alt="plus">
    </div>
  </div>
</template>