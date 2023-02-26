<script lang="ts" setup>
import { MenuItemsList } from '@/features'
import { pizzas, beer } from './consts.js'
</script>

<template>
  <div class="menu-wrap">
    <MenuItemsList title="Pizza" :items="pizzas" />
    <MenuItemsList title="Beer" :items="beer" />
  </div>
</template>

<style scoped>
.menu-wrap {
  position: relative;
  display: flex;
  flex-direction: column;
  gap: 40px;
  width: 100%;
}
</style>
