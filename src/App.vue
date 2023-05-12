<script setup>
import { RouterLink, RouterView } from "vue-router";
import NavBar from "./components/NavBar.vue";
</script>

<template>
  <div class="app">
    <NavBar />
    <RouterView />
  </div>
</template>

<style>
.app {
  width: 90vw;
  max-width: 100%;
  height: 100vh;
}
</style>
