	<script setup>
import { reactive } from 'vue'

const user = reactive({
  username: '',
  password: ''
})

const onLogin = () => {
  const { username, password } = user
  console.log('onLogin: ', username, password)
}
</script>
 
<template>
  <div class="mx-4">
    <form @submit.prevent="onLogin">
      <div class="grid grid-cols-[100px_1fr] gap-2 items-center mx-4">
        <label for="username-input">帳號: </label>
        <input
          class="border-b-4 border-gray-700 rounded-sm p-2"
          id="username-input"
          type="text"
          v-model="user.username"
        />

        <label for="password-input" class="ml-10">密碼: </label>
        <input
          class="border-b-4 border-gray-700 rounded-sm p-2"
          id="password-input"
          type="text"
          v-model="user.password"
        />
      </div>

      <div class="text-center mt-2">
        <button
          class="bg-green-500 text-white px-4 py-2 rounded-sm transition hover:brightness-105"
        >
          登入
        </button>
      </div>
    </form>
  </div>
</template>