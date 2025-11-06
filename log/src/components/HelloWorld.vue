<script setup lang="ts">
import SignInForm from './SignInForm.vue'
</script>

<template >
  <div class="flex h-screen w-full">
    <div class=" hidden md:block  md:w-1/2 bg-[#F8EAFF] p-8 flex flex-col justify-between items-center">
      <div class="w-full">
        <img src="/src/assets/logo.png" alt="logo" class="h-14 mb-6" />
      </div>

      <div class="w-full flex-1 flex items-center justify-center">
        <div class="max-w-xl text-center">
          <img
            src="/src/assets/cover.png"
            alt="people"
            class="w-full rounded-2xl shadow-md object-cover"
            style="height:380px;width:600px;"
          />

          <h3 class="mt-6 text-[#61227D] font-semibold text-lg">Team Achieve</h3>
          <p class="mt-2 text-[#5E5E5E]">Your perfect solution for funding your&nbsp;desires</p>
        </div>
      </div>

      <div class="w-full text-center text-sm text-gray-500">&nbsp;</div>
    </div>

    <div class="w-full md:w-1/2  px-5 md:px-12 flex items-center justify-center">
      <SignInForm />
    </div>
  </div>
</template>

<style scoped>
.app-wrap { height: 100%; }
</style>
