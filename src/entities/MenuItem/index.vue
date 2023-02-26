<script lang="ts" setup>
import type { Props } from './types'

const props = withDefaults(defineProps<Props>(), {
  name: 'Food Name',
  ingredients: 'Pepperoni, tomatoes, cheese, cheese, cheese something else...',
  price: '10.59$',
  image: null
})
</script>

<template>
  <div class="card">
    <img v-if="props.image" :src="props.image" alt="food" />
    <div v-else class="image"></div>
    <div class="description">
      <p class="name">{{ props.name }}</p>
      <p class="ingredients">{{ props.ingredients }}</p>
      <p class="price">{{ props.price }}</p>
    </div>
  </div>
</template>

<style lang="scss" scoped></style>
