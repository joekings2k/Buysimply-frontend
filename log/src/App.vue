<script setup lang="ts">
import HelloWorld from "./components/HelloWorld.vue";
</script>

<template>
  <!-- full-viewport two-panel layout -->
  <div class="min-h-screen w-screen flex">
    <HelloWorld />
  </div>
</template>

<style scoped>
/* small helpers kept local */
.app-wrap {
  height: 100%;
}
</style>
