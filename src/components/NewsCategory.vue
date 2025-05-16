<template>
  <div class="nav">
    <button
      v-for="cat in categories"
      :key="cat"
      @click="() => handleClick(cat)"
    >
      {{ cat }}
    </button>
  </div>
</template>

<script setup>
const categories = ["전체", "정치", "경제", "사회", "문화", "과학"];
const emit = defineEmits(["select"]);
const handleClick = (cat) => {
  console.log(cat);
  emit("select", cat);
};
</script>

<style scoped>
.nav {
  display: flex;
  gap: 0.5rem;
  padding: 1rem;
  border-bottom: 1px solid #ddd;
}
button {
  padding: 0.5rem 1rem;
  background-color: #eee;
  border: none;
  border-radius: 4px;
  cursor: pointer;
  flex-grow: 1;
}
button:hover {
  background-color: #ddd;
}
</style>
