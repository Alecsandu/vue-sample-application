<script setup lang="ts">
  import VibeTitle from './components/VibeTitle.vue';
  import VibeChecker from './components/VibeChecker.vue';
</script>

<template>
  <header>
    <VibeTitle/>
  </header>
  <main class="background">
    <VibeChecker/>
  </main>
</template>

<style lang="css" scoped>
  .background {
    background-image: linear-gradient(in lch, rgb(72, 35, 167), rgb(67, 3, 90));
  }
</style>
