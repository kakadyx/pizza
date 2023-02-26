<script lang="ts" setup>
import type { MenuItemProps } from './types'

const props = withDefaults(defineProps<MenuItemProps>(), {
  name: 'Food Name',
  ingredients: 'Pepperoni, tomatoes, cheese, cheese, cheese and something else...',
  price: '10.59$',
  image: null
})
</script>

<template>
  <div class="card">
    <img v-if="props.image" :src="props.image" alt="food" />
    <div v-else class="image">{{ props.name.split(' ').at(-1) }}</div>
    <div class="description">
      <p class="name">{{ props.name }}</p>
      <p class="ingredients">{{ props.ingredients }}</p>
      <p class="price">{{ props.price }}</p>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.card {
  display: flex;
  flex-direction: column;
  max-width: 250px;
  gap: 10px;
}
.image {
  width: 250px;
  height: 250px;
  background: blueviolet;
  color: white;
  font-size: 100px;
  font-weight: 600;
  display: flex;
  justify-content: center;
  align-items: center;
}
.description {
  display: flex;
  flex-direction: column;
  gap: 5px;
  .ingredients {
    font-size: 14px;
    color: var(--subparagraph);
    font-style: italic;
  }
  .name {
    font-size: 20px;
  }
  .price {
    font-size: 18px;
    font-weight: 600;
  }
}
</style>
