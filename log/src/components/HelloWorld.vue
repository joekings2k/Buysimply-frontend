<script setup lang="ts">
import SignInForm from './SignInForm.vue'
</script>

<template>
  <div class="flex h-full w-full app-wrap">
    <!-- LEFT: image + branding -->
    <div class="w-1/2 bg-purple-50 p-8 flex flex-col justify-between items-center">
      <div class="w-full">
        <img src="/src/assets/vue.svg" alt="logo" class="h-14 mb-6" />
      </div>

      <div class="w-full flex-1 flex items-center justify-center">
        <div class="max-w-md text-center">
          <img
            src="https://images.unsplash.com/photo-1524504388940-b1c1722653e1?q=80&w=1000&auto=format&fit=crop&ixlib=rb-4.0.3&s=3a0b4b7b5d4a6f0b9f9b9ee3a2b2a3a4"
            alt="people"
            class="w-full rounded-2xl shadow-md object-cover"
            style="height:260px"
          />

          <h3 class="mt-6 text-purple-800 font-semibold text-lg">Team Achieve</h3>
          <p class="mt-2 text-gray-600">Your perfect solution for funding your&nbsp;desires</p>
        </div>
      </div>

      <div class="w-full text-center text-sm text-gray-500">&nbsp;</div>
    </div>

    <!-- RIGHT: sign-in form -->
    <div class="w-1/2 p-12 flex items-center justify-center">
      <SignInForm />
    </div>
  </div>
</template>

<style scoped>
.app-wrap { height: 100%; }
</style>
