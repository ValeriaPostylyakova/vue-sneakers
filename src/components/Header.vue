<template>
  <header class="flex justify-between border-b border-slate-300 p-8">
    <div class="flex items-center gap-4">
      <img src="/logo.png" alt="logo" class="w-10">
      <div>
        <h2 class="text-xl font-bold">VUE SNEAKERS</h2>
        <p class="text-slate-400">Магазин лучших кроссовок</p>
      </div>
    </div>
  
    <ul class="flex items-center gap-10">
      <li class="flex items-center gap-3 text-gray-500 hover:text-black cursor-pointer">
        <img src="/cart.svg" alt="card">
        <b>1205 руб.</b>
      </li>
      <li class="flex items-center gap-3 text-gray-500 hover:text-black cursor-pointer">
        <img src="/heart.svg" alt="card">
        <span>Закладки</span>
      </li>
      <li class="flex items-center gap-3 text-gray-500 hover:text-black cursor-pointer">
        <img src="/profile.svg" alt="card">
        <span>Профиль</span>
      </li>
    </ul>
  </header>
</template>