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
  <v-card width="100%">
    <v-card-title>Дополните профиль</v-card-title>
    <v-card-text>
      <v-form v-model="form" @submit.prevent="onSubmit">
        <div class="input">
          <span>Имя</span>
          <v-text-field
            bg-color="#F5F5F5"
            placeholder="Ваше имя"
            variant="text"
          ></v-text-field>
        </div>
        <div class="input">
          <span>Почта</span>
          <v-text-field
            bg-color="#F5F5F5"
            placeholder="Ваша электронная почта"
            variant="text"
          ></v-text-field>
        </div>
        <div class="input">
          <span>Смена пароля</span>
          <v-text-field
            bg-color="#F5F5F5"
            placeholder="Нынешний пароль"
            variant="text"
          ></v-text-field>
          <v-text-field
            bg-color="#F5F5F5"
            placeholder="Новый пароль"
            variant="text"
          ></v-text-field>
          <v-text-field
            bg-color="#F5F5F5"
            placeholder="Повтор нового пароля"
            variant="text"
          ></v-text-field>
        </div>
        <div class="buttons">
          <v-btn size="x-large" style="color: #000" variant="text"
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
</style>
