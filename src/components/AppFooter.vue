<template>
  <v-footer>
    <div class="main-container">
      <div class="main-footer">
        <div class="column align-center flex-row">
          <Logo />
        </div>
        <div class="column">
          <div class="column-title">Контакт</div>
          <div class="column-items">
            <div class="column-item">
              Б. Грузинская ул., 42, <br />20, Москва, 123056
            </div>
            <div class="column-item">
              <a href="tel:+79182034355"></a>+7 918 203 43 55
            </div>
            <div class="column-item">
              <a href="mailto:contact@crediwayonline.com"
                >contact@crediwayonline.com</a
              >
            </div>
          </div>
        </div>
        <div class="column">
          <div class="column-title">Аккаунт</div>
          <div class="column-items">
            <div class="column-item">
              <RouterLink>
                <div class="link">Вход / Регистрация</div></RouterLink
              >
            </div>
            <div class="column-item">
              <RouterLink to="/lk">
                <div class="link">Личный кабинет</div></RouterLink
              >
            </div>
          </div>
        </div>
        <div class="column">
          <div class="column-title">Организация</div>
          <div class="column-items">
            <div class="column-item">
              <RouterLink>
                <div class="link">Правила и условия</div></RouterLink
              >
            </div>
            <div class="column-item">
              <RouterLink>
                <div class="link">Политика конфиденциальности</div></RouterLink
              >
            </div>
            <div class="column-item">
              <RouterLink>
                <div class="link">Пользовательское соглашение</div></RouterLink
              >
            </div>
            <div class="column-item">
              <RouterLink> <div class="link">О нас</div></RouterLink>
            </div>
          </div>
        </div>
      </div>
      <div class="little-footer">
        <svg
          xmlns="http://www.w3.org/2000/svg"
          width="19"
          height="20"
          viewBox="0 0 19 20"
          fill="none"
        >
          <path
            d="M9.50002 18.3334C14.1024 18.3334 17.8334 14.6025 17.8334 10.0001C17.8334 5.39771 14.1024 1.66675 9.50002 1.66675C4.89765 1.66675 1.16669 5.39771 1.16669 10.0001C1.16669 14.6025 4.89765 18.3334 9.50002 18.3334Z"
            stroke="white"
            stroke-width="1.5"
            stroke-linecap="round"
            stroke-linejoin="round"
          />
          <path
            d="M12 8.14823C12 8.14823 10.9706 6.66675 9.25492 6.66675C7.53924 6.66675 6.16669 8.14823 6.16669 10.0001C6.16669 11.8519 7.53924 13.3334 9.25492 13.3334C10.9706 13.3334 12 11.8519 12 11.8519"
            stroke="white"
            stroke-width="1.5"
            stroke-linecap="round"
            stroke-linejoin="round"
          />
        </svg>
        <span>Copyright Rimel 2022. All right reserved</span>
      </div>
    </div>
  </v-footer>
</template>

<script setup></script>
<style lang="scss" scoped>
footer {
  padding: 0;
  background-color: #000;
  .main-footer {
    padding: 80px 0 100px;
    display: flex;
    justify-content: space-between;
    .column {
      display: flex;
      flex-direction: column;
      justify-content: flex-start;
      align-items: flex-start;
      gap: 24px;
      color: #fafafa;
      .column-title {
        font-size: 20px;
        font-style: normal;
        font-weight: 500;
        line-height: 28px; /* 140% */
      }
      .column-items {
        display: flex;
        flex-direction: column;
        gap: 16px;

        .column-item {
          font-size: 16px;
          font-style: normal;
          font-weight: 500;
          line-height: 24px; /* 150% */
          .link {
            @include textLinkWhite;
          }
        }
      }
    }
  }
  .little-footer {
    opacity: 0.5;
    padding: 16px 0;
    display: flex;
    justify-content: center;
    align-items: center;
    color: #fff;
    gap: 6px;
    font-size: 16px;
    font-style: normal;
    font-weight: 400;
    line-height: 24px; /* 150% */
    svg {
      margin-right: 10px;
    }
  }
}
</style>
