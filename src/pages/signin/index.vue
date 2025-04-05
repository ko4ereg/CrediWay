<script setup>
import { ref } from "vue";

const form = ref(null);

const onSubmit = () => {
  if (!form.value) {
    return false;
  }
};
</script>

<template>
  <div class="main-container">
    <div class="container d-flex justify-end">
      <div class="sideimage"></div>
      <div class="form">
        <div class="titles">
          <div class="title">Вход в аккаунт</div>
          <div class="subtitle">Введите данные ниже</div>
        </div>
        <v-form class="w-100" v-model="form" @submit.prevent="onSubmit">
          <v-text-field
            bg-color="transparent"
            placeholder="Номер телефона"
            variant="underlined"
          ></v-text-field>

          <v-text-field
            bg-color="transparent"
            placeholder="Пароль"
            variant="underlined"
          ></v-text-field>

          <div class="buttons">
            <v-btn
              type="submit"
              size="x-large"
              style="color: #fafafa"
              color="#D5A57D"
              >Войти</v-btn
            >
            <div class="recovery">
              <RouterLink to="/recovery">
                <div class="link red">Забыли пароль?</div></RouterLink
              >
            </div>
          </div>
        </v-form>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.container {
  margin-top: 60px;
  margin-bottom: 100px;
  position: relative;
  height: 60dvh;
}
.sideimage {
  border-radius: 0px 4px 4px 0px;
  position: absolute;
  left: -55%;
  height: 706px;
  width: 100%;
  background: #cbe4e8 url("@/assets/authBack.jpg") 130% bottom / contain
    no-repeat;
}

.form {
  display: flex;
  flex-direction: column;
  align-items: flex-start;
  gap: 48px;
  padding-top: 193px;
  width: 40%;

  .titles {
    display: flex;
    flex-direction: column;
    align-items: flex-start;
    gap: 24px;

    color: #000;

    .title {
      font-family: "Inter";
      font-size: 36px;
      font-style: normal;
      font-weight: 500;
      line-height: 30px; /* 83.333% */
      letter-spacing: 1.44px;
    }

    .subtitle {
      font-size: 16px;
      font-style: normal;
      font-weight: 400;
      line-height: 24px; /* 150% */
    }
  }

  .buttons {
    display: flex;

    gap: 16px;
    justify-content: space-between;
    margin-top: 40px;
    .v-btn {
      text-transform: none;

      font-size: 16px;
      font-style: normal;
      font-weight: 500;
      line-height: 24px; /* 150% */
    }
    .recovery {
      display: flex;
      align-items: center;
      gap: 16px;
      color: #000;

      font-size: 16px;
      font-style: normal;
      font-weight: 400;
      line-height: 24px; /* 150% */
      opacity: 0.7;
      .link {
        @include textLink;
        font-weight: 500;
      }

      .red {
        color: red;
        &:before {
          background: red;
        }
      }
    }
  }
}
</style>
