<script lang="ts" setup>
import { MenuItem } from '@/entities'
import type { MenuItemsListProps } from './types'
const props = withDefaults(defineProps<MenuItemsListProps>(), {
  title: 'Default title',
  items: () => [
    {
      price: 'price',
      name: 'name',
      ingredients: 'ingredients',
      image: null
    },
    {
      price: 'price',
      name: 'name',
      ingredients: 'ingredients',
      image: null
    },
    {
      price: 'null',
      name: 'null',
      ingredients: 'null',
      image: null
    },
    {
      price: 'price',
      name: 'name',
      ingredients: 'ingredients',
      image: null
    },
    {
      price: 'price',
      name: 'name',
      ingredients: 'ingredients',
      image: null
    },
    {
      price: 'price',
      name: 'name',
      ingredients: 'ingredients',
      image: null
    }
  ]
})
</script>
<template>
  <div class="item-list">
    <h4 class="submenu-header">{{ props.title }}</h4>
    <div class="items-wrap">
      <MenuItem
        v-for="(item, i) in props.items"
        :key="i"
        :image="item.image"
        :ingredients="item.ingredients + i"
        :name="item.name + ' ' + i"
        :price="item.price + i"
      />
    </div>
  </div>
</template>

<style lang="scss" scoped>
.item-list {
  display: flex;
  gap: 20px;
}
.items-wrap {
  width: 100%;
  display: flex;
  flex-wrap: wrap;
  justify-content: space-between;
  gap: 20px;
}
.submenu-header {
  font-size: 35px;
  font-weight: 700;
  margin-bottom: 10px;
}
</style>
