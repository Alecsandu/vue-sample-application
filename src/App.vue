<script setup lang="ts">
  import { ref } from 'vue';

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
      <div v-if="vibePass">
        <video width="320" height="180" autoplay>
          <source src="/goat.mp4" type="video/mp4">
          Your browser does not support the video tag.
        </video>
      </div>
      <div v-if="vibeImprove">
        <video width="320" height="180" autoplay>
          <source src="/qeres.mp4" type="video/mp4">
          Your browser does not support the video tag.
        </video>
      </div>
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

  video {
    border: 0px;
    border-radius: 5%;
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
