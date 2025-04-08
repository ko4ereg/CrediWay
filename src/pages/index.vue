<script setup>
//
</script>

<template>
  <div class="main-container">
    <div class="main-page">
      <div class="main-page_sidebar">
        <div class="main-page_links">
          <RouterLink target="_blank" to="/"> <div class="main-page_link">Контакты</div></RouterLink>
          <RouterLink target="_blank"  to="/">
            <div class="main-page_link">Правила и условия</div></RouterLink
          >
          <RouterLink target="_blank" to="/">
            <div class="main-page_link">
              Политика конфиденциальности
            </div></RouterLink
          >
          <RouterLink target="_blank" to="/"> 
            <div class="main-page_link">
              Пользовательское соглашение
            </div></RouterLink
          >
        </div>
      </div>
      <div class="main-page_greeting">
        <div class="title">Получай кешбеки за оплату сервисов в интернете</div>
        <div class="text">
          Совершаешь покупку с <span>Wildberries/Ozon</span> на 10,000 рублей,
          делишься своим мнением о товаре - и магазин благодарит тебя бонусами
          на 100 рублей. А дальше ещё интереснее: эти бонусы моментально
          превратились в подарочный сертификат! Просто покупай, делись
          впечатлениями и получай приятные бонусы!
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.main-container {
  height: 100%;
}
.main-page {
  height: 100dvh;
  display: flex;
  .main-page_sidebar {
    padding: 40px 14px 0 0;
    border-right: 1px solid rgba(0, 0, 0, 0.3);
    .main-page_links {
      display: flex;
      flex-direction: column;
      align-items: flex-start;
      gap: 16px;
      .main-page_link {
        @include textLink;
        text-align: start;
        text-wrap: nowrap;
      }
    }
  }
  .main-page_greeting {
    padding: 55px 0 0 62px;
    display: flex;
    flex-direction: column;
    gap: 57px;
    align-items: start;
    .title {
      color: #2f2f2f;

      /* Heading/48PX SemiBold */
      font-family: "Inter";
      font-size: 48px;
      font-style: normal;
      font-weight: 600;
      line-height: 60px; /* 125% */
      letter-spacing: 1.92px;
    }

    .text {
      width: 60%;
      color: #8a8a8a;
      font-family: "Roboto";
      font-size: 20px;
      font-style: normal;
      font-weight: 500;
      line-height: 171%; /* 34.2px */
      span {
        font-weight: 700;
      }
    }
  }
}

@media (max-width: 1439px) {
  .main-container {
    height: 70dvh;
  }

  .main-page {
    .main-page_sidebar {
      .main-page_links {
        .main-page_link {
          font-size: 1rem;
        }
      }
    }
    .main-page_greeting {
      padding: 55px 0 0 62px;
      display: flex;
      flex-direction: column;
      gap: 57px;
      align-items: start;
      .title {
        font-size: 2rem;
        line-height: 40px; /* 125% */
        letter-spacing: 1.22px;
      }

      .text {
        width: 100%;
        font-size: 1rem;
        span {
          font-weight: 700;
        }
      }
    }
  }
}

@media (max-width: 767px) {
  .main-container {
    height: auto;
    padding-bottom: 20px;
  }
  .main-page {
    flex-direction: column;
    .main-page_sidebar {
      border-right: none;
      order: 2;
      .main-page_links {
        .main-page_link {
          font-size: 1rem;
        }
      }
    }
    .main-page_greeting {
      padding: 15px 0 0 0px;

      .title {
        font-size: 2rem;
        line-height: 40px; /* 125% */
        letter-spacing: 1.22px;
      }

      .text {
        width: 100%;
        font-size: 1rem;
        span {
          font-weight: 700;
        }
      }
    }
  }
}
</style>
