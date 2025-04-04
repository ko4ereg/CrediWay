<script setup>
//
</script>

<template>
  <div class="main-container">
    <div class="main-page">
      <div class="main-page_sidebar">
        <div class="main-page_links">
          <RouterLink> <div class="main-page_link">Контакты</div></RouterLink>
          <RouterLink>
            <div class="main-page_link">Правила и условия</div></RouterLink
          >
          <RouterLink>
            <div class="main-page_link">
              Политика конфиденциальности
            </div></RouterLink
          >
          <RouterLink>
            <div class="main-page_link">
              Пользовательское соглашение
            </div></RouterLink
          >
        </div>
      </div>
      <div class="main-page_greeting">
        <div class="title">Получай кешбеки за оплату сервисов в интернете</div>
        <div class="text">
          Совершаешь покупку с Wildberries/Ozon на 10,000 рублей, делишься своим
          мнением о товаре - и магазин благодарит тебя бонусами на 100 рублей. А
          дальше ещё интереснее: эти бонусы моментально превратились в
          подарочный сертификат! Просто покупай, делись впечатлениями и получай
          приятные бонусы!
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
  height: 100%;
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
  }
}
</style>
