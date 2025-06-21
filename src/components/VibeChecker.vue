<script setup lang="ts">
  import { ref } from 'vue';
  import VideoVibe from './VideoVibe.vue';

  const vibePass = ref(false);
  const vibeImprove = ref(false);

  const vibeDo = () => {
    vibePass.value = !vibePass.value;
    vibeImprove.value = false;
  };

  const vibeDont = () => {
    vibePass.value = false;
    vibeImprove.value = !vibeImprove.value;
  };
</script>

<template>
  <section class="checker-main-background">
    <div class="checker-secondary-background">
      <span class="checker-title">Vibe check ✅</span>
      <span class="checker-question">is you vibing bro?</span>
      <div class="buttons">
        <button class="btn1" @click="vibeDo">Type shii 🔥</button>
        <button class="btn2" @click="vibeDont">Nah fam 🥀</button>
      </div>
      <div>
        <VideoVibe v-if="vibePass" :videoName="'goat.mp4'" />
        <VideoVibe v-if="vibeImprove" :videoName="'qeres.mp4'" />
      </div>
    </div>
  </section>
</template>

<style lang="css" scoped>
  .checker-main-background {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    min-height: 100vh;
  }

  .checker-secondary-background {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    text-align: center;
    background-image: linear-gradient(in lch, rgb(157, 112, 225), rgb(83, 36, 146));
    border-radius: 15px;
    padding: 0.2rem;
  }

  .checker-title {
    margin: 1.2rem;
    font-size: 2.5rem;
    padding-bottom: 1rem;
    font-weight: bold;
  }

  .checker-question {
    font-size: 2rem;
    font-weight: bold;
    text-align: center;
  }

  .buttons {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: row;
  }

  .btn1 {
    border-radius: 15px;
    font-size: 1.5rem;
    border: 0px;
    padding: 0.2rem;
    margin: 0.5rem;
    background-color: rgb(32, 201, 26);
    font-weight: bold;
  }

  .btn2 {
    border-radius: 15px;
    font-size: 1.5rem;
    border: 0px;
    padding: 0.2rem;
    margin: 0.5rem;
    font-style: italic;
    background-color: gray;
  }
</style>
