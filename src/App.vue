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
  <header>
    <div class="wrapper">
      <h1>Vibe check ✅</h1>
      <span id="spanid">is you vibing bro?</span>
      <div>
        <button class="btn1" @click="vibeDo">Type shii 🔥</button>
        <button class="btn2" @click="vibeDont">Nah fam 🥀</button>
      </div>
      <VideoVibe v-if="vibePass" :videoName="'/goat.mp4'" />
      <VideoVibe v-if="vibeImprove" :videoName="'/qeres.mp4'" />
    </div>
  </header>
</template>

<style scoped>
  header {
    display: flex;
    flex-direction: column;
    align-items: center;
    justify-content: center;
    min-height: 100vh;
    padding: 20px;
  }
  .wrapper {
    text-align: center;
    background-image: linear-gradient(rgb(123, 83, 183), rgb(83, 36, 146));
    border-radius: 25%;
    padding: 2rem;
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

    #spanid {
      font-size: 2rem;
      font-weight: bold;
    }
</style>
