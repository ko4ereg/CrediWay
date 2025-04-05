<script setup>
import { ref } from "vue";
import { useDisplay } from "vuetify";

const form = ref(false);
const formSms = ref(false);
const { width } = useDisplay();
const phone = ref("");
const password = ref("");
const passwordRepeat = ref("");
const smsCode = ref("");
const snackbar = ref(false);
const error = ref(false);

const submitSignUp = ref(false);
const submitSms = ref(false);
const onSubmit = () => {
  if (!form.value) {
    return;
  }
  submitSignUp.value = true;
};
const smsSubmit = () => {
  if (!formSms.value) {
    return;
  }
  submitSms.value = true;
};
</script>

<template>
  <div class="main-container">
    <div class="container d-flex justify-end">
      <div v-if="width > 767" class="sideimage"></div>
      <div class="form">
        <div class="titles">
          <div class="title">Регистрация</div>
          <div class="subtitle">Введите данные ниже</div>
        </div>
        <v-form
          style="height: 420px"
          v-if="!submitSignUp"
          class="w-100"
          v-model="form"
          @submit.prevent="onSubmit"
        >
          <v-text-field
            bg-color="transparent"
            placeholder="Телефон"
            variant="underlined"
          ></v-text-field>

          <v-text-field
            bg-color="transparent"
            placeholder="Пароль"
            variant="underlined"
          ></v-text-field>

          <v-text-field
            bg-color="transparent"
            placeholder="Повтор пароля"
            variant="underlined"
          ></v-text-field>

          <div class="buttons">
            <v-btn
              type="submit"
              size="x-large"
              style="color: #fafafa"
              color="#D5A57D"
              >Создать аккаунт</v-btn
            >
            <div class="signin">
              <span>Уже есть аккаунт?</span>
              <RouterLink to="/signin">
                <div class="link">Войти</div></RouterLink
              >
            </div>
          </div>
        </v-form>
        <v-form
          style="height: 420px"
          v-else
          class="w-100"
          v-model="formSms"
          @submit.prevent="smsSubmit"
        >
          <div class="titles">
            <div class="subtitle">
              Регистрация прошла успешно, вам придет SMS-сообщение с кодом на
              указанный номер телефона в течении 24 часов
            </div>
          </div>

          <v-text-field
            bg-color="transparent"
            placeholder="SMS-код"
            variant="underlined"
          ></v-text-field>

          <div class="buttons">
            <v-btn
              type="submit"
              size="x-large"
              style="color: #fafafa"
              color="#D5A57D"
              >Подтвердить аккаунт</v-btn
            >
            <div class="signin">
              <span>Уже есть аккаунт?</span>
              <RouterLink to="/signin">
                <div class="link">Войти</div></RouterLink
              >
            </div>
          </div>
        </v-form>
        <div class="agrees">
          <div class="agree">
            <v-icon>mdi-check</v-icon>
            <router-link
              ><span>Согласие на получение СМС-оповещений</span>
            </router-link>
          </div>
          <div class="agree">
            <v-icon>mdi-check</v-icon>
            <router-link
              ><span>Согласие на обработку персональных данных</span>
            </router-link>
          </div>
        </div>
      </div>
    </div>
  </div>

  <v-snackbar timeout="3000" color="error" v-model="error">
    {{ errorMessage }}

    <template v-slot:actions>
      <v-btn color="white" variant="text" @click="snackbar = false">
        <v-icon>mdi-close</v-icon>
      </v-btn>
    </template>
  </v-snackbar>
</template>

<style lang="scss" scoped>
.container {
  margin-top: 60px;
  margin-bottom: 100px;
  position: relative;
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
  padding-top: 100px;
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
    flex-direction: column;
    gap: 16px;
    justify-content: flex-end;
    margin-top: 40px;
    .v-btn {
      text-transform: none;

      font-size: 16px;
      font-style: normal;
      font-weight: 500;
      line-height: 24px; /* 150% */
    }
    .signin {
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
    }
  }
  .agrees {
    margin-top: 30px;
    display: flex;
    flex-direction: column;
    gap: 27px;
    .agree {
      display: flex;
      gap: 14px;
      align-items: center;
      span {
        transition: 0.2s ease-out;
        color: #000;
        font-size: 16px;
        font-style: normal;
        font-weight: 500;
        line-height: 24px; /* 150% */
        opacity: 0.5;

        @media (hover: hover) and (pointer: fine) {
          &:hover {
            text-decoration: underline;
          }
        }

        @media (hover: none) and (pointer: coarse) {
          &:active {
            text-decoration: underline;
          }
        }
      }
    }
  }
}
</style>
