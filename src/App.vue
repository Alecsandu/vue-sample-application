<script setup lang="ts">
  import { ref } from 'vue';
  import VideoVibe from './components/VideoVibe.vue';

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
  <div class="container-main">
    <div class="wrapper">
      <h1>Vibe check ✅</h1>
      <span class="spanQuestion">is you vibing bro?</span>
      <div class="buttons">
        <button class="btn1" @click="vibeDo">Type shii 🔥</button>
        <button class="btn2" @click="vibeDont">Nah fam 🥀</button>
      </div>
      <VideoVibe v-if="vibePass" :videoName="'/goat.mp4'" />
      <VideoVibe v-if="vibeImprove" :videoName="'/qeres.mp4'" />
    </div>
  </div>
</template>

<style scoped>
  .container-main {
    display: flex;
    justify-content: center;
    align-items: center;
    min-height: 100vh;
    background-image: linear-gradient(in lch, rgb(72, 35, 167), rgb(67, 3, 90));
  }
  
  .wrapper {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: column;
    text-align: center;
    background-image: linear-gradient(in lch, rgb(157, 112, 225), rgb(83, 36, 146));
    border-radius: 25%;
    padding: 2rem;
  }

  .buttons {
    display: flex;
    justify-content: center;
    align-items: center;
    flex-direction: row;
  }

  .btn1 {
    border-radius: 10px;
    font-size: 1.5rem;
    border: 0px;
    padding: 0.2rem;
    margin: 0.5rem;
    background-color: rgb(32, 201, 26);
    font-weight: bold;
  }

  .btn2 {
    border-radius: 10px;
    font-size: 1.5rem;
    border: 0px;
    padding: 0.2rem;
    margin: 0.5rem;
    font-style: italic;
    background-color: gray;
  }

  h1 {
    margin: 1.2rem;
    font-size: 2.5rem;
    padding-bottom: 1rem;
  }

  .spanQuestion {
    font-size: 2rem;
    font-weight: bold;
    text-align: center;
  }
</style>
