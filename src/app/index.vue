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
.app {
  min-height: 100vh;
  font-family: sans-serif;
  display: flex;
  flex-direction: column;
  & > * {
    padding-inline: var(--side-offset);
  }
}
</style>
