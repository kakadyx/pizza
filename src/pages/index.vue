<script setup lang="ts">
import { RouterView } from 'vue-router'
import { TheHeader, TheFooter } from '@/widgets'
</script>

<template>
  <TheHeader />
  <RouterView />
  <TheFooter />
</template>
