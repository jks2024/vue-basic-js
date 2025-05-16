<template>
  <NewsItem v-for="news in items" :key="news.title" :item="news" />
</template>

<script setup>
import NewsItem from "./NewsItem.vue";
const props = defineProps({
  items: Array,
});
</script>

<style scoped></style>
