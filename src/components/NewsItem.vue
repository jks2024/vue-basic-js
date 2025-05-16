<template>
  <div class="news-item">
    <img :src="item.image" :alt="item.title" class="thumb" />
    <div class="content">
      <h3>{{ item.title }}</h3>
      <p>{{ item.content }}</p>
      <p>{{ item.date }}</p>
    </div>
  </div>
</template>

<script setup>
const props = defineProps({
  item: Object,
});
</script>

<style scoped>
.news-item {
  display: flex;
  padding: 1rem;
  gap: 1rem;
  padding: 1rem;
  border-bottom: 1px solid #ccc;
}
.content {
  flex: 1;
}
.thumb {
  width: 120px;
  height: 120px;
  object-fit: cover;
  border-radius: 6px;
}
</style>
