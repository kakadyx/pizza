<script setup></script>

<template>
  <div class="content">
    <div class="filler"></div>
  </div>
</template>

<style lang="scss" scoped>
.content {
  display: flex;
  flex: 1;
  overflow: auto;
  .filler {
    height: 9999px;
  }

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
