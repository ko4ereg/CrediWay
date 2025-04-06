<script setup>
import { RouterView } from "vue-router";

//
</script>

<template>
  <div class="main-container">
    <div class="lk-header d-flex align-center justify-space-between">
      <div class="breadcrumbs">
        <RouterLink to="/"> <span>Главная</span></RouterLink> <span>/</span> ЛК
      </div>

      <div class="greeting">Добрый день! {{ name || "Безымянный" }}</div>
    </div>

    <div class="lk-main d-flex align-start h-100">
      <div class="sidebar">
        <div class="sidebar-title">Управление аккаунтом</div>
        <div class="sidebar-items">
          <div class="sidebar-item">
            <router-link active-class="active" to="/lk/info"
              >Личные данные</router-link
            >
          </div>
        </div>
      </div>
      <div class="lk-content"><RouterView /></div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.main-container {
  min-height: 90dvh;
  padding: 0 80px;
  display: flex;
  flex-direction: column;
  gap: 40px;
}
.lk-header {
  @include innerHeader;
}

.lk-main {
  gap: 10%;
  .sidebar {
    color: #000;
    font-size: 16px;
    font-style: normal;
    font-weight: 500;
    line-height: 24px; /* 150% */
    display: flex;
    flex-direction: column;
    gap: 16px;
    .sidebar-items {
      display: flex;
      flex-direction: column;
      gap: 16px;
      font-weight: 400;
      align-items: center;
    }
  }
  .lk-content {
    flex: 1 1 auto;
  }
}

.active {
  color: #d5a57d;
  transition: 0.2s ease-out;
  &:hover {
    color: #b49479;
  }
}

@media (max-width: 1419px) {
  .main-container {
    padding-bottom: 40px;
  }
}

@media (max-width: 1023px) {
  .main-container {
    padding: 40px 40px;
  }
}

@media (max-width: 767px) {
  .main-container {
    padding: 10px 20px;

    flex-direction: column;
    gap: 20px;
  }
  .lk-header {
    @include innerHeader;
    padding: 10px 0px;
  }

  .lk-main {
    gap: 20px;
    flex-direction: column;
    .lk-content {
      width: 100%;
    }
    .sidebar {
      flex-direction: column;
      gap: 16px;
    }
  }
}
</style>
