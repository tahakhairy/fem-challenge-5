<template>
  <div class="app">
    <navbar @open-menu="(value) => (isOpen = value)" />

    <main-section />

    <modal-menu
      :isOpen="isOpen"
      @close-menu="(value) => (isOpen = value)"
    ></modal-menu>
  </div>
</template>

<script setup>
import { ref } from "vue";
import Navbar from "./components/Navbar.vue";
import MainSection from "./components/MainSection.vue";
import ModalMenu from "./components/ModalMenu.vue";

const isOpen = ref(false);
</script>

<style scoped>
.app {
  margin: 4rem 0;
}
@media (max-width: 600px) {
  .app {
    position: relative;
    width: 100%;
    height: 100vh;
  }
}
</style>
