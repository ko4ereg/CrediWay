<script setup>
import Logo from "./Logo.vue";
</script>

<template>
  <v-app-bar absolute app height="142" location="top" elevation="0">
    <div class="main-container">
      <div class="d-flex align-end header">
        <RouterLink to="/"> <Logo /> </RouterLink>
        <div class="links">
          <RouterLink> <div class="link">Главная</div></RouterLink>
          <RouterLink> <div class="link">О нас</div></RouterLink>
          <RouterLink> <div class="link">Вход / Регистрация</div></RouterLink>
        </div>
      </div>
    </div>
  </v-app-bar>
</template>

<style scoped lang="scss">
.v-app-bar {
  border-bottom: 1px solid rgba(0, 0, 0, 0.3);
  height: auto;
  :deep(.v-toolbar__content) {
    height: auto !important;
  }
}
.header {
  gap: 10%;
  padding: 80px 0 20px;
  .links {
    display: inline-flex;
    gap: 54px;
    .link {
      @include textLink;
    }
  }
}
</style>
