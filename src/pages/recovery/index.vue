<script setup>
import { required } from "@/utils/validator";
import { ref } from "vue";

const form = ref(null);
const phone = ref("");
const smsCode = ref("");
const submitPhoneSuccess = ref(false);
const submitSMSSuccess = ref(false);

const time = ref(60);

const timer = () => {
  if (time.value > 0) {
    time.value--;
  } else {
    clearInterval(timerId.value);
  }
};

const timerId = ref(null);

const onSubmit = () => {
  if (!form.value) {
    return false;
  }
  submitPhoneSuccess.value = true;
  timerId.value = setInterval(timer, 1000);
};
const submitSMS = () => {
  if (!smsCode.value) {
    return false;
  }
  submitSMSSuccess.value = true;
  clearInterval(timerId.value);
};

const snackbar = ref(false);
const formPass = ref(false);
const password = ref("");
const passwordRepeat = ref("");
const recoverySuccess = ref(false);
const submitRecovery = () => {
  if (!formPass.value) {
    return false;
  }
  recoverySuccess.value = true;
  snackbar.value = true;
};

const passwordsMatch = (value) => {
  return !!value === password.value || "Пароли не совпадают";
};

const loading = ref(false);
</script>

<template>
  <div class="main-container">
    <div class="container d-flex justify-end">
      <div class="sideimage"></div>
      <div class="form">
        <div class="titles">
          <div class="title">Восстановление</div>
          <div class="subtitle">Введите данные ниже</div>
        </div>
        <v-form
          v-if="!submitSMSSuccess"
          class="w-100"
          v-model="form"
          validate-on="submit"
          @submit.prevent="onSubmit"
        >
          <v-text-field
            validate-on="lazy input"
            v-model="phone"
            :rules="[required]"
            bg-color="transparent"
            placeholder="Номер телефона"
            variant="underlined"
          ></v-text-field>
          <v-text-field
            v-if="submitPhoneSuccess"
            v-model="smsCode"
            bg-color="transparent"
            placeholder="Код"
            variant="underlined"
          ></v-text-field>

          <div class="buttons">
            <v-btn
              :loading="loading"
              v-if="!submitPhoneSuccess"
              type="submit"
              size="x-large"
              style="color: #fafafa"
              color="#D5A57D"
              >Прислать проверочный код</v-btn
            >
            <span v-if="submitPhoneSuccess"
              >Если код не пришел, можете запросить отправку повторно через
              {{ time }}</span
            >
            <v-btn
              :loading="loading"
              v-if="submitPhoneSuccess"
              type="submit"
              :disabled="time > 0"
              size="x-large"
              style="color: #fafafa"
              color="#D5A57D"
              >Прислать проверочный код повторно</v-btn
            >
            <v-btn
              :loading="loading"
              :disabled="!smsCode"
              v-if="submitPhoneSuccess"
              @click="submitSMS"
              type="submit"
              size="x-large"
              style="color: #fafafa"
              color="#D5A57D"
              >Подтвердить</v-btn
            >
          </div>
        </v-form>
        <v-form
          v-else
          class="w-100"
          v-model="formPass"
          @submit.prevent="submitRecovery"
        >
          <v-text-field
            :rules="[required]"
            v-model="password"
            bg-color="transparent"
            placeholder="Новый пароль"
            variant="underlined"
          ></v-text-field>
          <v-text-field
            :rules="[passwordsMatch]"
            v-model="passwordRepeat"
            bg-color="transparent"
            placeholder="Повтор пароля"
            variant="underlined"
          ></v-text-field>

          <div class="buttons">
            <v-btn
              :loading="loading"
              :disabled="recoverySuccess"
              type="submit"
              size="x-large"
              style="color: #fafafa"
              color="#D5A57D"
              >Сохранить</v-btn
            >
            <RouterLink to="/signin"> <div class="link">Войти</div></RouterLink>
          </div>
        </v-form>
      </div>
    </div>
  </div>

  <v-snackbar timeout="3000" color="success" v-model="snackbar">
    Пароль успешно изменен

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
    flex-direction: column;
    justify-content: space-between;
    margin-top: 40px;
    .v-btn {
      text-transform: none;

      font-size: 16px;
      font-style: normal;
      font-weight: 500;
      line-height: 24px; /* 150% */
    }

    .link {
      @include textLink;
      font-weight: 500;
      width: fit-content;
    }
  }
}

@media (max-width: 1023px) {
  .container {
    height: 80dvh;
  }
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
  .sideimage {
    display: none;
  }

  .v-form {
    height: 420px;
  }
  .form {
    padding-bottom: 100px;
    width: 100%;

    .buttons {
      margin-top: 10px;
    }
    .agrees {
      margin-top: 0px;
    }
  }
}
</style>
