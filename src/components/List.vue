<script setup>
import CardMain from './CardMain.vue';

const onClickAdd = () => {
    
};
</script>

<template>
    <div class="grid grid-cols-4 gap-5">
        <CardMain
         img-url="./sneakers/sneakers-1.jpg"
          :price="12999"
           title="Мужские Кроссовки Nike Blazer Mid Suede"
           :is-added="false"
           :isLike="true"
           :onClickAdd="onClickAdd"
           />
        <CardMain/>
        <CardMain/>
        <CardMain/>
        <CardMain/>
    </div>
</template>