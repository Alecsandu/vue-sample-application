<script setup lang="ts">
    defineProps<{
      videoName: string
    }>()
</script>

<template>
    <video width="320" height="180" autoplay>
        <source :src="videoName" type="video/mp4">
        <p>Your browser does not support the video tag.</p>
    </video>
</template>

<style lang="css" scoped>
  video {
    border: 0px;
    border-radius: 5%;
  }
</style>