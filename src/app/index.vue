<script setup lang="ts">
import { Routing } from '@/pages'
</script>

<template>
  <div class="app">
    <Routing />
  </div>
</template>

<style lang="scss">
@import '@/app/style/reset.scss';
@import '@/app/style/variables.scss';
@import '@/app/style/main.scss';
.app {
  min-height: 100vh;
  max-height: 100vh;
  font-family: sans-serif;
  display: flex;
  flex-direction: column;
  & > * {
    margin-inline: var(--side-offset);
  }
}
</style>
