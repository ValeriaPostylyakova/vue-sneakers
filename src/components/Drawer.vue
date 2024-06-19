<script setup>
import DrawerHead from './DrawerHead.vue';
import CartItemList from './CartItemList.vue';
</script>

<template>
  <div class="fixed top-0 left-0 h-full w-full bg-black z-10 opacity-70"></div>
  <div class="fixed right-0 top-0 bg-white w-96 h-full z-20 p-8">
    <DrawerHead/>
    <CartItemList/>

    <div class="mt-10">
      <div class="flex gap-2 mb-4">
        <span>Итого:</span>
        <div class="flex-1 border-b bprder-dashed "></div>
        <b>12900 руб.</b>
      </div>
      <div class="flex gap-2">
        <span>Налог 5%:</span>
        <div class="flex-1 border-b bprder-dashed"></div>
        <b>1074 руб.</b>
      </div>
    </div>
    <button
    disabled=""
     class="cursor-pointer disabled:bg-slate-400 bg-lime-500 w-full rounded-2xl mt-5 py-3 text-white hover:bg-lime-600 transition active:bg-lime-700">Оформить заказ</button>
  </div>
</template>