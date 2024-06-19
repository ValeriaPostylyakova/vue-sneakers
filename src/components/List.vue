<script setup>
import CardMain from './CardMain.vue';

defineProps({
    items: Array
});
</script>

<template>
    <div class="grid grid-cols-4 gap-5">
        <CardMain
        v-for="item in items"
          :key="item.id"
          :image-url="item.imageUrl"
          :title="item.title"
          :price="item.price"
          :onClickAdd="onClickAdd"/>
    </div>
</template>