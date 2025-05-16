<template>
  <div class="container">
    <h2>회원 정보</h2>
    <UserItem v-for="user in users" :key="user.name" :user="user" />
  </div>
</template>

<script setup>
import { reactive, onMounted } from "vue";
import UserItem from "../components/UserItem.vue";
const users = reactive([]);

const fetchedData = [
  { name: "장원영", age: 20, address: "서울 강남구", isAdult: true },
  { name: "안유진", age: 19, address: "서울 마포구", isAdult: false },
  { name: "김민지", age: 22, address: "부산 해운대구", isAdult: true },
  { name: "최수빈", age: 17, address: "인천 연수구", isAdult: false },
  { name: "이도현", age: 25, address: "대구 수성구", isAdult: true },
  { name: "박소영", age: 16, address: "경기 고양시", isAdult: false },
  { name: "윤지후", age: 30, address: "광주 북구", isAdult: true },
  { name: "한서진", age: 21, address: "서울 동작구", isAdult: true },
  { name: "정지훈", age: 18, address: "대전 유성구", isAdult: false },
  { name: "강채영", age: 23, address: "울산 남구", isAdult: true },
];

// 화면이 처음 나타나는 시점
onMounted(() => {
  // 서버로 데이터를 요청하고 데이터가 전달 되면 아래의 동작 수행
  users.push(...fetchedData);
});
</script>
<style scoped>
.container {
  width: 500px;
  margin: 40px auto;
  text-align: center;
  background-color: antiquewhite;
}
</style>
