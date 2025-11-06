<template>
  <div class="w-full flex items-center justify-center  ">
    <form
      @submit.prevent="handleSubmit"
      class="w-full p-8 rounded-lg shadow-sm space-y-6"
    >
      <h2 class="text-3xl text-purple-800 font-semibold text-center">
        Welcome Back
      </h2>
      <p class="text-center text-gray-600">
        Enter your email address and password to access your account.
      </p>
      <!-- Email -->
      <div>
        <label class="block text-gray-700 font-medium mb-1"
          >Email Address <span class="text-red-500">*</span></label
        >
        <input
          type="email"
          v-model="email"
          placeholder="Enter your email"
          required
          class="w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 bg-white focus:ring-purple-600"
        />
      </div>

      <!-- Password -->
      <div>
        <label class="block text-gray-700 font-medium mb-1"
          >Password <span class="text-red-500">*</span></label
        >
        <div class="relative">
          <input
            :type="showPassword ? 'text' : 'password'"
            v-model="password"
            placeholder="Enter your password"
            required
            class="bg-white  w-full px-3 py-2 border border-gray-300 rounded-md focus:outline-none focus:ring-2 focus:ring-purple-600 pr-10"
          />
          <button
            type="button"
            @click="showPassword = !showPassword"
            class="absolute right-3 top-1/2 -translate-y-1/2 text-gray-500 hover:text-gray-700"
          >
            <svg
              v-if="!showPassword"
              xmlns="http://www.w3.org/2000/svg"
              class="h-5 w-5"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M15 12a3 3 0 11-6 0 3 3 0 016 0z"
              />
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M2.458 12C3.732 7.943 7.523 5 12 5c4.478 0 8.268 2.943 9.542 7-1.274 4.057-5.064 7-9.542 7-4.477 0-8.268-2.943-9.542-7z"
              />
            </svg>
            <svg
              v-else
              xmlns="http://www.w3.org/2000/svg"
              class="h-5 w-5"
              fill="none"
              viewBox="0 0 24 24"
              stroke="currentColor"
            >
              <path
                stroke-linecap="round"
                stroke-linejoin="round"
                stroke-width="2"
                d="M13.875 18.825A10.05 10.05 0 0112 19c-4.478 0-8.268-2.943-9.542-7a9.964 9.964 0 012.308-3.944M9.88 9.88a3 3 0 104.24 4.24M3 3l18 18"
              />
            </svg>
          </button>
        </div>
      </div>

      <!-- Remember me + Forgot password -->
      <div class="flex items-center justify-between text-sm">
        <label class="flex items-center space-x-2 text-gray-600">
          <input
            type="checkbox"
            v-model="remember"
            class="rounded border-gray-300 "
          />
          <span>Remember me</span>
        </label>
        <a href="#" class="text-purple-700 hover:underline">Forgot Password?</a>
      </div>

      <!-- Submit Button -->
      <button
        type="submit"
        class="w-full bg-purple-700 hover:bg-purple-800 text-white font-semibold py-3 rounded-md transition-colors"
      >
        Sign in
      </button>

      <!-- Sign up link -->
      <p class="text-center text-sm text-gray-600">
        Don’t have an account?
        <a href="#" class="text-purple-700 font-semibold hover:underline"
          >Sign up</a
        >
      </p>
    </form>
  </div>
</template>

<script setup>
import { ref } from "vue";

const email = ref("");
const password = ref("");
const remember = ref(false);
const showPassword = ref(false);

const handleSubmit = () => {
  console.log({
    email: email.value,
    password: password.value,
    remember: remember.value,
  });
};
</script>
