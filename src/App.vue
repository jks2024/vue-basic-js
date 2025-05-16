<script setup>
import DataBiding from "./components/DataBiding.vue";
import ConditionRender from "./components/ConditionRender.vue";
import Iterable from "./components/IterableArray.vue";
import ClassBiding from "./components/ClassBiding.vue";
import Reactive from "./components/Reactive.vue";
import Computed from "./components/Computed.vue";
import Watch from "./components/Watch.vue";
import TemplateTotal from "./components/TemplateTotal.vue";
import CardView from "./components/CardView.vue";
import UserCard from "./pages/UserCard.vue";
import ChildComponent from "./components/ChildComponent.vue";
import News from "./pages/News.vue";
import EventRef from "./components/EventRef.vue";
import SignUp from "./pages/Signup.vue";
import EventHandle from "./components/EventHandle.vue";
import SelectBox from "./components/SelectBox.vue";
import ArrayRender from "./components/ArrayRender.vue";
//import { ref } from "vue";
// const message = ref("");

// const handleMessage = (payload) => {s
//   message.value = payload;
// };
</script>

<template>
  <!-- <h3>App.vue 영역 입니다.</h3> -->
  <!-- <input v-model="member.name" placeholder="이름 입력" />
  <br />
  <input v-model="member.job" placeholder="직업" />
  <br />
  <input v-model.number="member.age" placeholder="나이" /> -->

  <!-- <DataBiding /> -->
  <!-- <ConditionRender /> -->
  <!-- <Iterable /> -->
  <!-- <ClassBiding /> -->
  <!-- <Reactive /> -->
  <!-- <Computed /> -->
  <!-- <Watch /> -->
  <!-- <TemplateTotal /> -->
  <!-- <CardView :user="member" /> -->
  <!-- <UserCard /> -->
  <!-- <h2>부모 컴포넌트</h2>
  <p>자식에게 받은 메시지: {{ message }}</p>
  <ChildComponent @send-message="handleMessage" /> -->
  <!-- <News /> -->
  <!-- <EventRef /> -->
  <!-- <SignUp /> -->
  <!-- <EventHandle /> -->
  <!-- <SelectBox /> -->
  <ArrayRender />
</template>

<style scoped>
h1 {
  font-size: 24x;
  color: royalblue;
}
input {
  padding: 8px;
  font-size: 18px;
  margin-top: 10px;
}
</style>
