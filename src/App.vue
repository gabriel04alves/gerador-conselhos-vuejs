<script setup>
import FooterDefault from './components/FooterDefault.vue';
import HeaderDefault from './components/HeaderDefault.vue';
</script>
<template>
  <link href="assets/my-style.css" rel="stylesheet">
  <HeaderDefault/>
  <RouterView class="main" />
  <FooterDefault/>
</template>

<style scoped>
.main {
  height: 50rem;
}
</style>
