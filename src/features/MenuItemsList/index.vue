<script lang="ts" setup>
import { MenuItem } from '@/entities'
import type { MenuItemsListProps } from './types'
const props = withDefaults(defineProps<MenuItemsListProps>(), {
  items: () => [
    {
      price: 'null',
      name: 'null',
      ingredients: 'null',
      image: null
    },
    {
      price: 'null',
      name: 'null',
      ingredients: 'null',
      image: null
    },
    {
      price: 'null',
      name: 'null',
      ingredients: 'null',
      image: null
    },
    {
      price: 'null',
      name: 'null',
      ingredients: 'null',
      image: null
    },
    {
      price: 'null',
      name: 'null',
      ingredients: 'null',
      image: null
    },
    {
      price: 'null',
      name: 'null',
      ingredients: 'null',
      image: null
    }
  ],
  title: 'Default title'
})
</script>
<template>
  <div>
    <h4 class="submenu-header">{{ props.title }}</h4>
    <div class="items-wrap">
      <MenuItem
        v-for="(item, i) in items"
        :key="i"
        :image="item.image"
        :ingredients="item.ingredients"
        :name="item.name"
        :price="item.price"
      />
    </div>
  </div>
</template>

<style scoped></style>
