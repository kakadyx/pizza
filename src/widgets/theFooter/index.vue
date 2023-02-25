<script setup></script>

<template>
  <footer class="footer">
    <hr class="separator" />
    <div class="content">
      <div class="contacts">
        <span class="company-name">COMPANY NAME 2023</span>
        <a class="link" href="#">Контакты</a>
        <a class="link" href="#">Правовая информация</a>
      </div>
      <div class="social-links">
        <a class="link" href="#">INST</a>
        <a class="link" href="#">VK</a>
        <a class="link" href="#">TG</a>
      </div>
    </div>
  </footer>
</template>

<style lang="scss" scoped>
.footer {
  padding-bottom: 20px;
  display: flex;
  flex-direction: column;
  justify-content: space-between;
  align-items: center;
  gap: 10px;
}

.content {
  width: 100%;
  display: flex;
  justify-content: space-between;
  align-items: center;
}
.contacts {
  display: flex;
  gap: 30px;
  font-size: 20px;

  a {
    color: var(--paragraph);
    cursor: pointer;
  }
  .link {
    text-decoration: none;
  }
  .company-name {
    color: var(--title);
  }
}

.social-links {
  width: fit-content;
  display: flex;
  gap: 10px;
  justify-content: space-between;
  font-size: 16px;
  .link {
    background: black;
    color: white;
    display: flex;
    align-items: center;
    padding: 10px;
    border-radius: 5px;
    text-decoration: none;
    font-weight: 600;
  }
}
</style>
