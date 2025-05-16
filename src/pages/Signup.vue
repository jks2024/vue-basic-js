<template>
  <div class="form-container">
    <h2>회원가입</h2>
    <form @submit.prevent="handleSubmit">
      <div class="form-group">
        <label>아이디</label>
        <input v-model="form.email" type="text" required />
      </div>

      <div class="form-group">
        <label>비밀번호</label>
        <input v-model="form.password" type="password" required />
      </div>

      <div class="form-group">
        <label>비밀번호 확인</label>
        <input v-model="form.confirmPassword" type="password" required />
      </div>

      <div class="form-group">
        <label>이름</label>
        <input v-model="form.name" type="text" required />
      </div>

      <button type="submit" :disabled="!isFormValid">가입하기</button>
    </form>
  </div>
</template>

<script setup>
import { reactive, computed } from "vue";
import axios from "axios";

const form = reactive({
  email: "",
  password: "",
  confirmPassword: "",
  name: "",
});

const isFormValid = computed(() => {
  return (
    form.email.trim() !== "" &&
    form.password.trim() !== "" &&
    form.confirmPassword.trim() !== "" &&
    form.name.trim() !== "" &&
    form.password === form.confirmPassword
  );
});

const handleSubmit = async () => {
  try {
    const payload = {
      email: form.email,
      pwd: form.password,
      name: form.name,
    };
    const res = await axios.post(
      "http://222.117.237.119:8111/auth/signup",
      payload
    );
    if (res.data) {
      alert("회원 가입 성공");
    } else {
      alert("회원 가입 실패");
    }
  } catch (err) {
    console.error(err);
    alert("가입 실패! 서버 오류 발생");
  }
};
</script>

<style scoped>
.form-container {
  max-width: 400px;
  margin: 40px auto;
  padding: 20px;
  border: 1px solid #ccc;
  border-radius: 8px;
  background: #f9f9f9;
  font-family: sans-serif;
}
h2 {
  margin-bottom: 1rem;
}
.form-group {
  margin-bottom: 1rem;
}
label {
  display: block;
  margin-bottom: 0.5rem;
  font-weight: bold;
}
input {
  width: 96%;
  padding: 0.5rem;
  border: 1px solid #ccc;
  border-radius: 4px;
}
button {
  padding: 0.5rem 1rem;
  background: #007bff;
  color: white;
  border: none;
  border-radius: 4px;
  cursor: pointer;
}
button:disabled {
  background: #ccc;
  cursor: not-allowed;
}
button:hover:enabled {
  background: #0056b3;
}
</style>
