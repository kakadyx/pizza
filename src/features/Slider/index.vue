<script lang="ts" setup>
import { ref, computed } from 'vue'
const items = [1, 2, 3, 4, 5, 6, 7, 8]
const currentSlide = ref(0)
const cssVars = computed(() => `--track-offset: ${-(currentSlide.value * 100)}%`)
let handleMode = false

const intervalId = setInterval(() => {
  if (currentSlide.value < items.length - 1) currentSlide.value++
}, 2000)
const paginateNext = () => {
  if (!handleMode) {
    handleMode = true
    clearInterval(intervalId)
  }
  if (currentSlide.value < items.length - 1) currentSlide.value++
}
const paginatePrev = () => {
  if (!handleMode) {
    handleMode = true
    clearInterval(intervalId)
  }
  if (currentSlide.value > 0) currentSlide.value--
}
</script>

<template>
  <div class="slider-container">
    <div :style="cssVars" class="slider-track">
      <div v-for="i in items" :key="i" class="slide">SLIDE {{ i }}</div>
    </div>
    <div class="pagination">
      <div class="prev" @click="paginatePrev" v-if="currentSlide !== 0" />
      <div class="next" @click="paginateNext" v-if="currentSlide !== items.length - 1" />
    </div>
  </div>
</template>

<style lang="scss" scoped>
.slider-container {
  width: 100%;
  overflow: hidden;
  position: relative;
}

.slider-track {
  display: flex;
  transition: 0.5s all;
  --track-offset: 0%;
  transform: translateX(var(--track-offset));
}

.slide {
  flex-shrink: 0;
  width: 100%;
  background: crimson;
  color: white;
  font-size: 56px;
  font-weight: 600;
  padding: 50px 100px;
  height: 300px;
  display: flex;
  justify-content: center;
  align-items: center;
}

.pagination {
  position: absolute;
  inset: 0;
  .prev {
    cursor: pointer;
    position: absolute;
    width: 20px;
    height: 20px;
    top: 50%;
    left: 30px;
    transform: translateY(-50%) rotate(-45deg);
    border-top: 4px solid white;
    border-left: 4px solid white;
  }
  .next {
    cursor: pointer;
    position: absolute;
    width: 20px;
    height: 20px;
    top: 50%;
    right: 30px;
    transform: translateY(-50%) rotate(45deg);
    border-top: 4px solid white;
    border-right: 4px solid white;
  }
}
</style>
