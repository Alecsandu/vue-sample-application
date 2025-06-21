<script setup lang="ts">
  import VibeTitle from './components/VibeTitle.vue';
  import VibeChecker from './components/VibeChecker.vue';
  import { SignedIn, SignedOut, SignInButton, UserButton } from '@clerk/vue';
</script>

<template>
  <SignedOut>
    <header>
      <VibeTitle/>
      <SignInButton />
    </header>
  </SignedOut>
  <SignedIn>
    <main class="background">
      <VibeChecker/>
      <UserButton />
    </main>
  </SignedIn>
</template>

<style lang="css" scoped>
  .background {
    background-image: linear-gradient(in lch, rgb(72, 35, 167), rgb(67, 3, 90));
  }
</style>
