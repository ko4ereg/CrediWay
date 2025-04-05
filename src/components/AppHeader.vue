<script setup>
import { useDisplay } from "vuetify";
import Logo from "./Logo.vue";
const { width } = useDisplay();
</script>

<template>
  <v-app-bar
    absolute
    app
    :height="width < 768 ? 64 : 142"
    location="top"
    elevation="0"
  >
    <div class="main-container">
      <div class="d-flex align-end header">
        <RouterLink to="/"> <Logo /> </RouterLink>
        <div class="links">
          <RouterLink to="/" active-class="active">
            <div class="link">Главная</div></RouterLink
          >
          <RouterLink to="/about" active-class="active">
            <div class="link">О нас</div></RouterLink
          >
          <RouterLink to="/signup" active-class="active">
            <div class="link">Вход / Регистрация</div></RouterLink
          >
        </div>
      </div>
    </div>
  </v-app-bar>
</template>

<style scoped lang="scss">
.v-app-bar {
  border-bottom: 1px solid rgba(0, 0, 0, 0.3);
  height: auto;
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
    .active {
      .link {
        &:before {
          content: "";
          position: absolute;
          height: 1px;
          bottom: 0;
          left: 15%;
          width: 75%;
          transform: scale(1);
          background: rgba(0, 0, 0, 0.5);
          transition: transform 0.25s ease-out;
        }
      }
    }
  }
}

@media (max-width: 767px) {
  .header {
    gap: 15px;
    padding: 0px 0 0px;
    .links {
      display: inline-flex;
      gap: 15px;
    }
  }
}
@media (max-width: 393px) {
  .header {
    gap: 10px;
    padding: 0px 0 0px;
    .links {
      display: inline-flex;
      gap: 5px;
    }
  }
}
</style>
