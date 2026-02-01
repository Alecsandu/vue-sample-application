<script setup lang="ts">
    defineProps<{
      videoName: string
    }>()
</script>

<template>
    <video autoplay>
        <source :src="videoName" type="video/mp4">
        <p>Your browser does not support the video tag.</p>
    </video>
</template>

<style lang="css" scoped>
  video {
    border: 0;
    margin: 0;
    width: 16rem;
    height: auto;
    border-radius: 50%;
  }
</style>
