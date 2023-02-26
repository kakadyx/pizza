<script setup></script>

<template>
  <header class="header">
    <div class="content">
      <div class="logo">
        <span>LOGO</span>
      </div>
      <div class="make-order">
        <a href="tel:+79998887766" class="phone-number">+7-999-888-77-66</a>
        <span class="text">Приём заказов с 9:00 до 23:00</span>
      </div>
    </div>

    <hr class="separator" />
  </header>
</template>

<style lang="scss" scoped>
.header {
  padding-top: 20px;
  display: flex;
  flex-direction: column;
  gap: 10px;
}

.content {
  display: flex;
  justify-content: flex-start;
  align-items: center;
  gap: 20px;
}

.logo {
  font-size: 40px;
  font-weight: 800;
  pointer-events: none;
  user-select: none;
}

.make-order {
  display: flex;
  flex-direction: column;
  gap: 5px;
  position: relative;
  .phone-number {
    text-decoration: none;
    color: var(--paragraph);
    font-weight: 600;
    font-size: 21px;
    width: fit-content;
    &::after {
      content: '';
      position: absolute;
      inset: 0;
      cursor: pointer;
    }
  }
  .text {
    color: var(--subparagraph);
    font-size: 14px;
    font-weight: 500;
  }
}
</style>
