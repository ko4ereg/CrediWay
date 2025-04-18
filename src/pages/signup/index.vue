<script setup>
import { required, requiredCheck } from "@/utils/validator";
import { ref } from "vue";
import { useDisplay } from "vuetify";

const form = ref(false);
const formSms = ref(false);
const { width } = useDisplay();
const phone = ref("");
const password = ref("");
const passwordRepeat = ref("");
const smsCode = ref("");

const error = ref(false);
const errorMessage = ref("");
const submitSignUp = ref(false);
const submitSms = ref(false);
const notifications = ref(false);
const agree = ref(false);
const onSubmit = () => {
  if (
    !phone.value ||
    !password.value ||
    !passwordRepeat.value ||
    !agree.value ||
    !notifications.value
  ) {
    error.value = true;
    errorMessage.value = "Заполните все поля";
    return;
  }

  if (password.value !== passwordRepeat.value) {
    error.value = true;
    errorMessage.value = "Пароли не совпадают";
    return;
  }
  if (phone.value.length < 10) {
    error.value = true;
    errorMessage.value = "Неверный номер телефона";
    return;
  }
  loading.value = true;

  submitSignUp.value = true;
  loading.value = false;
};
const smsSubmit = () => {
  if (!formSms.value) {
    return;
  }
  loading.value = true;
  submitSms.value = true;
  loading.value = false;
};

const passwordsMatch = (value) => {
  return value === password.value || "Пароли не совпадают";
};

const passwordRepeatField = ref(null);

const resetValidation = async () => {
  if (passwordRepeatField.value) {
    return passwordRepeatField.value.resetValidation();
  }
};
const loading = ref(false);
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
          validate-on="submit"
          v-if="!submitSignUp"
          class="w-100"
          v-model="form"
          @submit.prevent="onSubmit"
        >
          <v-text-field
            validate-on="lazy input"
            bg-color="transparent"
            placeholder="Телефон"
            variant="underlined"
            :rules="[required]"
            v-model="phone"
          ></v-text-field>

          <v-text-field
            validate-on="lazy input"
            bg-color="transparent"
            placeholder="Пароль"
            :rules="[required]"
            v-model="password"
            variant="underlined"
          ></v-text-field>

          <v-text-field
            ref="passwordRepeatField"
            @update:focused="resetValidation"
            v-model="passwordRepeat"
            bg-color="transparent"
            :rules="[required, passwordsMatch]"
            placeholder="Повтор пароля"
            variant="underlined"
          ></v-text-field>

          <div class="buttons">
            <v-btn
              :loadin="loading"
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
          <div class="agrees">
            <div class="agree">
              <v-checkbox
                validate-on="input"
                hide-details
                v-model="notifications"
                :rules="[requiredCheck]"
              >
                <template v-slot:label>
                  <RouterLink target="_blank" to="/"
                    ><span>Согласие на получение СМС-оповещений</span>
                  </RouterLink></template
                >
              </v-checkbox>
            </div>
            <div class="agree">
              <v-checkbox
                hide-details
                validate-on="input"
                v-model="agree"
                :rules="[requiredCheck]"
              >
                <template v-slot:label>
                  <RouterLink target="_blank" to="/"
                    ><span>Согласие на обработку персональных данных</span>
                  </RouterLink></template
                >
              </v-checkbox>
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
            :rules="[required]"
            bg-color="transparent"
            placeholder="SMS-код"
            variant="underlined"
            v-model="smsCode"
          ></v-text-field>

          <div class="buttons">
            <v-btn
              :loadin="loading"
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
      </div>
    </div>
  </div>

  <v-snackbar timeout="3000" color="error" v-model="error">
    {{ errorMessage }}

    <template v-slot:actions>
      <v-btn color="white" variant="text" @click="error = false">
        <v-icon>mdi-close</v-icon>
      </v-btn>
    </template>
  </v-snackbar>

  <v-snackbar timeout="3000" color="success" v-model="submitSms">
    Аккаунт подтвержден, можете совершить вход

    <template v-slot:actions>
      <v-btn color="white" variant="text" @click="submitSms = false">
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
    margin-bottom: 130px;
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

    .agree {
      display: flex;
      gap: 14px;
      align-items: center;
      :deep(.v-checkbox .v-selection-control) {
        min-height: auto !important;
      }
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

@media (max-width: 1023px) {
  .sideimage {
    border-radius: 0px 4px 4px 0px;
    position: absolute;
    left: -55%;
    height: 706px;
    width: 100%;
    background: #cbe4e8 url("@/assets/authBack.jpg") 190% bottom / 80% no-repeat;
  }
}
@media (max-width: 767px) {
  .container {
    margin-top: 0px;
    margin-bottom: 0px;
  }
  .form {
    padding-bottom: 100px;
    width: 100%;

    .buttons {
      margin-top: 10px;
      margin-bottom: 30px;
    }
    .agrees {
      margin-top: 0px;
      .agree {
        span {
          font-size: 0.8rem;
        }
      }
    }
  }
}
</style>
