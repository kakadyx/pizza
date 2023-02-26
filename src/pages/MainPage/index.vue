<script setup lang="ts">
import { Menu } from '@/widgets'
</script>

<template>
  <div class="content">
    <Menu />
  </div>
</template>

<style lang="scss" scoped>
.content {
  display: flex;
  flex: 1;
  overflow: auto;

  &::-webkit-scrollbar {
    width: 4px;

    background-color: transparent;
  }
  &::-webkit-scrollbar-thumb {
    background: #000;
    border-radius: 9999px;
  }
}
</style>
