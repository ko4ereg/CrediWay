<script setup>
import { required } from "@/utils/validator";
import { onMounted, ref } from "vue";

const form = ref(null);

const onSubmit = () => {
  if (!form.value) {
    return false;
  }

  if (newPassword.value !== repeatNewPassword.value) {
    return false;
  }
};

const name = ref("");
const originalName = ref("Безымянный");
const email = ref("");
const originalEmail = ref("test@test.com");
const currentPassword = ref("");
const newPassword = ref("");
const repeatNewPassword = ref("");
const passwordRepeatField = ref(null);
const resetValidation = async () => {
  if (passwordRepeatField.value) {
    return passwordRepeatField.value.resetValidation();
  }
};
const passwordsMatch = (value) => {
  return value === newPassword.value || "Пароли не совпадают";
};

onMounted(() => {
  name.value = originalName.value;
  email.value = originalEmail.value;
});

const resetForm = () => {
  name.value = originalName.value;
  email.value = originalEmail.value;
  currentPassword.value = "";
  newPassword.value = "";
  repeatNewPassword.value = "";
};
</script>

<template>
  <v-card width="100%">
    <v-card-title>Дополните профиль</v-card-title>
    <v-card-text>
      <v-form validate-on="submit" v-model="form" @submit.prevent="onSubmit">
        <div class="input">
          <span>Имя</span>
          <v-text-field
            variant="solo"
            bg-color="#F5F5F5"
            placeholder="Ваше имя"
            v-model="name"
          ></v-text-field>
        </div>
        <div class="input">
          <span>Почта</span>
          <v-text-field
            variant="solo"
            v-model="email"
            bg-color="#F5F5F5"
            placeholder="Ваша электронная почта"
          ></v-text-field>
        </div>
        <div class="input">
          <span>Смена пароля</span>
          <v-text-field
            variant="solo"
            v-model="currentPassword"
            bg-color="#F5F5F5"
            :rules="[required]"
            placeholder="Нынешний пароль"
            validate-on="lazy input"
          ></v-text-field>
          <v-text-field
            variant="solo"
            v-model="newPassword"
            validate-on="lazy input"
            :rules="[required]"
            bg-color="#F5F5F5"
            placeholder="Новый пароль"
          ></v-text-field>
          <v-text-field
            ref="passwordRepeatField"
            v-model="repeatNewPassword"
            @update:focused="resetValidation"
            bg-color="#F5F5F5"
            :rules="[required, passwordsMatch]"
            placeholder="Повтор нового пароля"
            variant="solo"
          ></v-text-field>
        </div>
        <div class="buttons">
          <v-btn
            @click="resetForm"
            size="x-large"
            style="color: #000"
            variant="text"
            >Сбросить</v-btn
          >
          <v-btn
            type="submit"
            size="x-large"
            style="color: #fafafa"
            color="#D5A57D"
            >Сохранить изменения</v-btn
          >
        </div>
      </v-form>
    </v-card-text>
  </v-card>
</template>

<style lang="scss" scoped>
.v-field--variant-solo,
.v-field--variant-solo-filled {
  box-shadow: none;
}
.v-card {
  padding: 40px 80px;
  display: flex;
  flex-direction: column;
  gap: 16px;
}
.v-card-title {
  padding: 0;
  color: #d5a57d;
  font-size: 20px;
  font-style: normal;
  font-weight: 500;
  line-height: 28px; /* 140% */
}
.v-card-text {
  padding: 0;
  display: flex;
  flex-direction: column;
  gap: 24px;
}
.buttons {
  display: flex;
  gap: 16px;
  justify-content: flex-end;

  .v-btn {
    text-transform: none;

    font-size: 16px;
    font-style: normal;
    font-weight: 500;
    line-height: 24px; /* 150% */
  }
}
.input {
  display: flex;
  flex-direction: column;
  gap: 8px;
  span {
    color: #000;
    font-size: 16px;
    font-style: normal;
    font-weight: 400;
    line-height: 24px; /* 150% */
  }
}

@media (max-width: 767px) {
  .v-card {
    padding: 25px 20px;
    display: flex;
    flex-direction: column;
    gap: 16px;
  }

  .buttons {
    flex-direction: column;
  }
}
</style>
