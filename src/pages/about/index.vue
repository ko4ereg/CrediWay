<script setup></script>

<template>
  <div class="main-container">
    <div class="about-header d-flex align-center justify-space-between">
      <div class="breadcrumbs">
        <RouterLink to="/"><span>Главная</span></RouterLink> <span>/</span> О
        нас
      </div>
    </div>

    <div class="lk-main d-flex align-start h-100">
      <div class="text-block">
        <div class="text-title">Наша история</div>

        <div class="text-text">
          <p>
            Мы — команда энтузиастов, которая верит в то, что каждая покупка
            может быть не только приятной, но и выгодной. Наша история началась
            с простой идеи: почему бы не наградить людей за то, что они уже
            делают каждый день? Ведь покупки — это не просто рутина, это способ
            выражения себя, заботы о близких и поддержки любимых брендов.
          </p>
          <p>
            Как все начиналось <br />
            В 2018 году несколько друзей, устав от однообразных программ
            лояльности, решили создать что-то особенное. Мы заметили, что
            большинство магазинов предлагают стандартные бонусы или кэшбэк, но
            мало кто действительно вдохновляет своих клиентов. Так появился наш
            сервис — платформа, которая не только вознаграждает за покупки, но и
            превращает этот процесс в настоящее приключение.
          </p>
          <p>
            Первый прототип был запущен в небольшом формате: мы сотрудничали с
            несколькими локальными магазинами и предлагали пользователям
            уникальные бонусы за отзывы о товарах. Идея быстро завоевала
            популярность, ведь люди любят делиться своими впечатлениями и
            получать за это благодарность.
          </p>
          <p>
            Что движет нами сегодня
            <br />
            Сегодня наш сервис вырос в полноценную экосистему, объединяющую
            тысячи пользователей и сотни партнеров. Мы работаем с крупнейшими
            магазинами и брендами, чтобы предложить вам максимально выгодные
            условия. Но главное — мы остаемся верны своей миссии: помогать людям
            находить лучшие товары, делиться честными отзывами и получать за это
            достойное вознаграждение.
          </p>
          <p>
            Наша философия <br />
            Мы верим, что доверие — это основа всего. Именно поэтому мы строим
            наши отношения с пользователями на принципах прозрачности, честности
            и взаимного уважения. Каждый ваш отзыв помогает другим покупателям
            сделать осознанный выбор, а каждая покупка — поддерживает любимые
            бренды. Мы просто добавляем немного магии, чтобы этот процесс стал
            еще приятнее.
          </p>
          <p>
            Почему выбирают нас? <br />
            Простота: Никаких сложных схем. Просто покупайте, пишите отзывы и
            получайте бонусы.<br />
            Выгода: Мы предлагаем одни из самых щедрых условий для наших
            пользователей.<br />
            Разнообразие: От маленьких локальных магазинов до крупных
            международных брендов — у нас есть предложения для всех.<br />
            Инновации: Мы постоянно развиваемся, внедряя новые технологии и
            улучшая ваш опыт.<br />
          </p>
          <p>
            Наши планы на будущее <br />
            Мы только начинаем свой путь. Впереди — расширение географии работы,
            новые партнерства и уникальные программы поощрений. Мы мечтаем о
            том, чтобы стать частью жизни каждого покупателя, который ценит
            качество, честность и выгоду.
          </p>
          <p>
            Присоединяйтесь к нам <br />
            Станьте частью нашего сообщества, где каждый ваш шаг в мире покупок
            приносит пользу. Мы рады видеть вас среди тех, кто меняет правила
            игры вместе с нами!
          </p>
        </div>
      </div>
      <div class="pic-block">
        <div class="pic"><LogoWhite class="logo" /></div>
      </div>
    </div>

    <div class="cards">
      <div class="card">
        <div class="icon">
          <div class="outerCircle">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="80"
              height="80"
              viewBox="0 0 80 80"
              fill="none"
            >
              <path
                opacity="0.3"
                d="M80 40C80 62.0914 62.0914 80 40 80C17.9086 80 0 62.0914 0 40C0 17.9086 17.9086 0 40 0C62.0914 0 80 17.9086 80 40ZM10.9071 40C10.9071 56.0675 23.9325 69.0929 40 69.0929C56.0675 69.0929 69.0929 56.0675 69.0929 40C69.0929 23.9325 56.0675 10.9071 40 10.9071C23.9325 10.9071 10.9071 23.9325 10.9071 40Z"
                fill="#2F2E30"
              />
              <circle cx="40" cy="40" r="29" fill="black" />
            </svg>
            <div class="innerCircle">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="36"
                height="32"
                viewBox="0 0 36 32"
                fill="none"
              >
                <path
                  d="M32.1416 1H25.4883L26.3216 9.33333C26.3216 9.33333 27.9883 11 30.4883 11C31.8006 11.0017 33.0684 10.524 34.0533 9.65667C34.1574 9.55938 34.235 9.43716 34.2787 9.30156C34.3224 9.16596 34.3309 9.02145 34.3033 8.88167L33.1266 1.83333C33.0873 1.60049 32.9668 1.38909 32.7865 1.23656C32.6062 1.08404 32.3778 1.00024 32.1416 1V1Z"
                  stroke="white"
                  stroke-width="2"
                />
                <path
                  d="M25.4883 1L26.3216 9.33333C26.3216 9.33333 24.6549 11 22.1549 11C19.6549 11 17.9883 9.33333 17.9883 9.33333V1H25.4883Z"
                  stroke="#FAFAFA"
                  stroke-width="2"
                />
                <path
                  d="M17.9886 1V9.33333C17.9886 9.33333 16.3219 11 13.8219 11C11.3219 11 9.65527 9.33333 9.65527 9.33333L10.4886 1H17.9886Z"
                  stroke="#FAFAFA"
                  stroke-width="2"
                />
                <path
                  d="M10.4883 1H3.8366C3.59993 0.999912 3.37089 1.08377 3.19023 1.23666C3.00957 1.38955 2.88899 1.60157 2.84994 1.835L1.67494 8.88333C1.64747 9.02311 1.65601 9.16758 1.69974 9.30315C1.74348 9.43873 1.82097 9.56095 1.92494 9.65833C2.4716 10.1417 3.69327 11.0017 5.48827 11.0017C7.98827 11.0017 9.65494 9.335 9.65494 9.335L10.4883 1.00167V1Z"
                  stroke="#FAFAFA"
                  stroke-width="2"
                />
                <path
                  d="M3 11V27.6667C3 28.5507 3.35119 29.3986 3.97631 30.0237C4.60143 30.6488 5.44928 31 6.33333 31H29.6667C30.5507 31 31.3986 30.6488 32.0237 30.0237C32.6488 29.3986 33 28.5507 33 27.6667V11"
                  stroke="#FAFAFA"
                  stroke-width="2"
                />
                <path
                  d="M22.7217 31.0001V21.0001C22.7217 20.116 22.3705 19.2682 21.7454 18.6431C21.1202 18.0179 20.2724 17.6667 19.3883 17.6667H16.055C15.171 17.6667 14.3231 18.0179 13.698 18.6431C13.0729 19.2682 12.7217 20.116 12.7217 21.0001V31.0001"
                  stroke="#FAFAFA"
                  stroke-width="2"
                  stroke-miterlimit="16"
                />
              </svg>
            </div>
          </div>
        </div>
        <div class="text">
          <div class="count">10.5k</div>
          <div class="text-text">Оставленных отзывов</div>
        </div>
      </div>
      <div class="card">
        <div class="icon">
          <div class="outerCircle">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="80"
              height="80"
              viewBox="0 0 80 80"
              fill="none"
            >
              <path
                opacity="0.3"
                d="M80 40C80 62.0914 62.0914 80 40 80C17.9086 80 0 62.0914 0 40C0 17.9086 17.9086 0 40 0C62.0914 0 80 17.9086 80 40ZM10.9071 40C10.9071 56.0675 23.9325 69.0929 40 69.0929C56.0675 69.0929 69.0929 56.0675 69.0929 40C69.0929 23.9325 56.0675 10.9071 40 10.9071C23.9325 10.9071 10.9071 23.9325 10.9071 40Z"
                fill="#2F2E30"
              />
              <circle cx="40" cy="40" r="29" fill="black" />
            </svg>
            <div class="innerCircle">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="40"
                height="40"
                viewBox="0 0 40 40"
                fill="none"
              >
                <path
                  d="M20.0003 37.2728C29.5397 37.2728 37.273 29.5395 37.273 20C37.273 10.4606 29.5397 2.72729 20.0003 2.72729C10.4608 2.72729 2.72754 10.4606 2.72754 20C2.72754 29.5395 10.4608 37.2728 20.0003 37.2728Z"
                  stroke="black"
                  stroke-width="2"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                />
                <path
                  d="M25.0914 14.547C24.762 13.9758 24.2834 13.505 23.707 13.1848C23.1305 12.8646 22.4777 12.7072 21.8186 12.7294H18.1823C17.2178 12.7294 16.2929 13.1124 15.611 13.7941C14.929 14.4759 14.5459 15.4005 14.5459 16.3647C14.5459 17.3288 14.929 18.2535 15.611 18.9353C16.2929 19.617 17.2178 20 18.1823 20H21.8186C22.783 20 23.708 20.383 24.3899 21.0648C25.0719 21.7465 25.455 22.6712 25.455 23.6354C25.455 24.5995 25.0719 25.5242 24.3899 26.2059C23.708 26.8877 22.783 27.2707 21.8186 27.2707H18.1823C17.5232 27.2929 16.8704 27.1354 16.2939 26.8153C15.7174 26.4951 15.2389 26.0242 14.9095 25.453"
                  stroke="black"
                  stroke-width="2.75"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                />
                <path
                  d="M20 8.18188V12.1213M20 27.8789V31.8182"
                  stroke="black"
                  stroke-width="2.75"
                  stroke-linecap="round"
                  stroke-linejoin="round"
                />
              </svg>
            </div>
          </div>
        </div>
        <div class="text">
          <div class="count">33k</div>
          <div class="text-text">Получено покупателями</div>
        </div>
      </div>
      <div class="card">
        <div class="icon">
          <div class="outerCircle">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="80"
              height="80"
              viewBox="0 0 80 80"
              fill="none"
            >
              <path
                opacity="0.3"
                d="M80 40C80 62.0914 62.0914 80 40 80C17.9086 80 0 62.0914 0 40C0 17.9086 17.9086 0 40 0C62.0914 0 80 17.9086 80 40ZM10.9071 40C10.9071 56.0675 23.9325 69.0929 40 69.0929C56.0675 69.0929 69.0929 56.0675 69.0929 40C69.0929 23.9325 56.0675 10.9071 40 10.9071C23.9325 10.9071 10.9071 23.9325 10.9071 40Z"
                fill="#2F2E30"
              />
              <circle cx="40" cy="40" r="29" fill="black" />
            </svg>
            <div class="innerCircle fill">
              <svg
                xmlns="http://www.w3.org/2000/svg"
                width="40"
                height="40"
                viewBox="0 0 40 40"
                fill="none"
              >
                <path
                  d="M11.667 11.6667V8.33339C11.667 7.36818 11.9464 6.42362 12.4714 5.6137C12.9965 4.80379 13.7447 4.16315 14.6258 3.76912C15.5069 3.37509 16.4832 3.24451 17.4369 3.39313C18.3906 3.54176 19.2809 3.96325 20.0003 4.60672C20.7197 3.96325 21.61 3.54176 22.5637 3.39313C23.5174 3.24451 24.4937 3.37509 25.3749 3.76912C26.256 4.16315 27.0042 4.80379 27.5292 5.6137C28.0543 6.42362 28.3336 7.36818 28.3337 8.33339V11.6667H30.8337C31.4967 11.6667 32.1326 11.9301 32.6014 12.399C33.0703 12.8678 33.3337 13.5037 33.3337 14.1667V30.8417C33.3337 32.3866 32.72 33.8682 31.6276 34.9606C30.5352 36.053 29.0535 36.6667 27.5087 36.6667H13.3337C11.5655 36.6667 9.86986 35.9643 8.61961 34.7141C7.36937 33.4639 6.66699 31.7682 6.66699 30.0001V14.1667C6.66699 13.5037 6.93038 12.8678 7.39922 12.399C7.86807 11.9301 8.50395 11.6667 9.16699 11.6667H11.667ZM22.7253 34.1667C22.0454 33.1914 21.6818 32.0306 21.6837 30.8417V14.1667H9.16699V30.0001C9.16699 30.5472 9.27477 31.089 9.48416 31.5946C9.69356 32.1001 10.0005 32.5594 10.3874 32.9463C10.7743 33.3332 11.2336 33.6402 11.7391 33.8496C12.2447 34.0589 12.7865 34.1667 13.3337 34.1667H22.7253ZM19.167 11.6667V8.33339C19.167 7.67035 18.9036 7.03446 18.4348 6.56562C17.9659 6.09678 17.33 5.83339 16.667 5.83339C16.004 5.83339 15.3681 6.09678 14.8992 6.56562C14.4304 7.03446 14.167 7.67035 14.167 8.33339V11.6667H19.167ZM21.667 11.6667H25.8337V8.33339C25.8337 7.81878 25.6749 7.31669 25.379 6.89566C25.0832 6.47463 24.6645 6.15517 24.1803 5.98089C23.6961 5.8066 23.1699 5.78599 22.6736 5.92186C22.1773 6.05773 21.7349 6.34346 21.407 6.74005C21.5753 7.24005 21.667 7.77672 21.667 8.33339V11.6667ZM24.1837 30.8417C24.1837 31.7236 24.534 32.5693 25.1575 33.1929C25.7811 33.8164 26.6268 34.1667 27.5087 34.1667C28.3905 34.1667 29.2362 33.8164 29.8598 33.1929C30.4833 32.5693 30.8337 31.7236 30.8337 30.8417V14.1667H24.1837V30.8417Z"
                  fill="white"
                />
              </svg>
            </div>
          </div>
        </div>
        <div class="text">
          <div class="count">45.5k</div>
          <div class="text-text">Ежемесячных покупок</div>
        </div>
      </div>
      <div class="card">
        <div class="icon">
          <div class="outerCircle">
            <svg
              xmlns="http://www.w3.org/2000/svg"
              width="80"
              height="80"
              viewBox="0 0 80 80"
              fill="none"
            >
              <path
                opacity="0.3"
                d="M80 40C80 62.0914 62.0914 80 40 80C17.9086 80 0 62.0914 0 40C0 17.9086 17.9086 0 40 0C62.0914 0 80 17.9086 80 40ZM10.9071 40C10.9071 56.0675 23.9325 69.0929 40 69.0929C56.0675 69.0929 69.0929 56.0675 69.0929 40C69.0929 23.9325 56.0675 10.9071 40 10.9071C23.9325 10.9071 10.9071 23.9325 10.9071 40Z"
                fill="#2F2E30"
              />
              <circle cx="40" cy="40" r="29" fill="black" />
            </svg>
            <div class="innerCircle fill">
              <svg
                fill="#ffffff"
                height="30px"
                width="30px"
                version="1.1"
                id="Capa_1"
                xmlns="http://www.w3.org/2000/svg"
                xmlns:xlink="http://www.w3.org/1999/xlink"
                viewBox="0 0 481 481"
                xml:space="preserve"
              >
                <g>
                  <g>
                    <path
                      d="M256.7,301.9h-27.5c-10,0-18.1-8.1-18.1-18.1s8.1-18.1,18.1-18.1h48.4c6.6,0,12-5.4,12-12c0-6.6-5.4-12-12-12h-22.7V225
			c0-6.6-5.4-12-12-12s-12,5.4-12,12v16.7h-1.7c-23.2,0-42.1,18.9-42.1,42.1s18.9,42.1,42.1,42.1h27.5c10,0,18.1,8.1,18.1,18.1
			s-8.1,18.1-18.1,18.1h-49.3c-6.6,0-12,5.4-12,12c0,6.6,5.4,12,12,12H231v17.1c0,6.6,5.4,12,12,12c6.6,0,12-5.4,12-12v-17.1h2
			c0.1,0,0.2,0,0.3,0c23-0.3,41.5-19.1,41.5-42.1C298.8,320.8,279.9,301.9,256.7,301.9z"
                    />
                    <path
                      d="M423.3,274.7c-12.6-29-30-57.1-52-83.4c-26.6-32-53.1-53.4-66.6-63.3l51-94.6c2.5-4.7,1.7-10.5-2.2-14.2
			C340.3,6.3,326.3,0,310.7,0c-14.3,0-27.4,5.4-38.8,10.2c-9,3.7-17.5,7.3-24.4,7.3c-2.1,0-3.9-0.3-5.7-1C218,7.8,199.7,2.4,182,2.4
			c-22.4,0-41.5,9-60.2,28.2c-3.9,4-4.5,10.3-1.4,15l55,83.1c-13.6,10.1-39.6,31.3-65.7,62.6c-21.9,26.3-39.4,54.4-52,83.4
			c-15.8,36.5-23.8,74.6-23.8,113.2c0,51.3,41.8,93.1,93.1,93.1h227c51.3,0,93.1-41.8,93.1-93.1
			C447.1,349.3,439.1,311.2,423.3,274.7z M146,40.6c11.6-10,22.7-14.4,36-14.4c14.2,0,30.2,4.8,51.5,12.7c4.4,1.6,9.1,2.4,13.9,2.4
			c11.7,0,22.9-4.6,33.6-9.1c10.3-4.3,20.1-8.4,29.6-8.4c4.6,0,11.1,0.8,19.3,6.6l-48,89.2h-83.6L146,40.6z M354,457H127
			c-38.1,0-69.1-31-69.1-69.1c0-64.1,23.5-124.9,69.7-180.7c29.2-35.3,58.9-57.2,67.9-63.6h89.8c9.1,6.3,38.7,28.3,67.9,63.6
			c46.3,55.8,69.7,116.5,69.7,180.7C423.1,426,392.1,457,354,457z"
                    />
                  </g>
                </g>
              </svg>
            </div>
          </div>
        </div>
        <div class="text">
          <div class="count">25k</div>
          <div class="text-text">Выплачено подарками</div>
        </div>
      </div>
    </div>
  </div>
</template>

<style lang="scss" scoped>
.main-container {
  min-height: 90dvh;
  padding: 0 80px;
  display: flex;
  flex-direction: column;
  gap: 40px;

  .cards {
    display: inline-flex;
    align-items: flex-start;
    gap: 30px;
    flex-wrap: wrap;
    margin-bottom: 60px;
    justify-content: space-between;
    .card {
      display: flex;
      padding: 30px 44px 30px 50px;
      justify-content: flex-end;
      align-items: center;
      border-radius: 4px;
      border: 1px solid rgba(0, 0, 0, 0.3);
      flex-direction: column;
      gap: 24px;
      transition: 0.2s ease-out;
      .icon {
        .outerCircle {
          position: relative;
          path {
            transition: 0.2s ease-out;
          }
          circle {
            transition: 0.2s ease-out;
            fill: black;
          }
          .innerCircle {
            position: absolute;
            top: 50%;

            left: 50%;
            transform: translate(-50%, -50%);
            path {
              transition: 0.2s ease-out;
              stroke: #fafafa;
            }
          }
        }
      }
      .text {
        display: flex;
        flex-direction: column;
        align-items: center;
        gap: 12px;
        color: #000;
        transition: 0.2s ease-out;
        .count {
          font-family: "Inter";
          font-size: 32px;
          font-style: normal;
          font-weight: 700;
          line-height: 30px; /* 93.75% */
          letter-spacing: 1.28px;
        }

        .text-text {
          text-align: center;
          font-size: 16px;
          font-style: normal;
          font-weight: 400;
          line-height: 24px; /* 150% */
        }
      }
      @media (hover: hover) and (pointer: fine) {
        &:hover {
          background: #db4444;

          box-shadow: 0px 2px 10px 2px rgba(0, 0, 0, 0.2);
          .icon {
            .outerCircle {
              path {
                fill: white;
              }
              circle {
                fill: white;
              }
              .innerCircle {
                position: absolute;
                top: 50%;
                svg {
                  fill: black;
                }
                left: 50%;
                transform: translate(-50%, -50%);
                path {
                  stroke: black;
                }
              }

              .fill {
                path {
                  fill: black;
                }
              }
            }
          }
          .text {
            color: white;
          }
        }
      }

      @media (hover: none) and (pointer: coarse) {
        &:active {
          background: #db4444;

          box-shadow: 0px 2px 10px 2px rgba(0, 0, 0, 0.2);
          .icon {
            .outerCircle {
              path {
                fill: white;
              }
              circle {
                fill: white;
              }
              .innerCircle {
                position: absolute;
                top: 50%;
                svg {
                  fill: black;
                }
                left: 50%;
                transform: translate(-50%, -50%);
                path {
                  stroke: black;
                }
              }

              .fill {
                path {
                  fill: black;
                }
              }
            }
          }
          .text {
            color: white;
          }
        }
      }
    }
  }
}
.lk-main {
  gap: 5%;
  .text-block {
    display: flex;
    flex-direction: column;
    gap: 40px;
    padding-top: 38px;
    .text-title {
      color: #000;
      text-align: justify;

      font-family: "Inter";
      font-size: 54px;
      font-style: normal;
      font-weight: 600;
      line-height: 64px; /* 118.519% */
      letter-spacing: 3.24px;
    }

    .text-text {
      color: #000;
      font-size: 16px;
      font-style: normal;
      font-weight: 400;
      line-height: 26px; /* 162.5% */
      display: flex;
      flex-direction: column;
      gap: 24px;
    }
  }
  .pic-block {
    flex: 1 0 40%;
    height: 100%;
    .pic {
      position: relative;
      width: auto;
      height: 609px;
      background: lightgray url("@/assets/aboutBack.png") 50% / cover no-repeat;
      border-radius: 4px 0px 0px 4px;
      right: -20%;
      .logo {
        left: 50%;
        transform: rotate(-6deg) translateX(-50%);
        position: absolute;
        top: 60%;
      }
    }
  }
}
.about-header {
  @include innerHeader;
  padding-bottom: 42px;
}

@media (max-width: 1023px) {
  .main-container {
    .cards {
      .card {
        width: 100%;
      }
    }
  }
  .lk-main {
    gap: 1%;
    flex-direction: column;
    .text-block {
      order: 2;

      padding-top: 0px;
    }
    .pic-block {
      width: 100%;

      order: 1;
      .pic {
        height: 300px;

        border-radius: 4px 4px 4px 4px;
        right: 0%;
      }
    }
  }
}
@media (max-width: 767px) {
  .main-container {
    padding: 0 20px;

    .cards {
      flex-direction: column;
      flex-wrap: wrap;
      align-items: center;
      .card {
        padding: 5px 10px 5px 10px;
        gap: 5px;

        .text {
          .count {
            font-family: "Inter";
            font-size: 1.5rem;
            font-style: normal;
            font-weight: 700;
            line-height: 30px; /* 93.75% */
            letter-spacing: 1.28px;
          }

          .text-text {
            text-align: center;
            font-size: 16px;
            font-style: normal;
            font-weight: 400;
            line-height: 24px; /* 150% */
          }
        }
      }
    }
  }
  .lk-main {
    .text-block {
      .text-title {
        font-size: 2rem;

        letter-spacing: 1.24px;
      }

      .text-text {
        text-align: justify;
      }
    }
    .pic-block {
      .pic {
        .logo {
          // scale: (0.7);
          font-size: 1rem;
        }
      }
    }
  }
  .about-header {
    @include innerHeader;
    padding-bottom: 42px;
  }
}
@media (max-width: 575px) {
  .lk-main {
    .pic-block {
      .pic {
        .logo {
          transform: rotate(-6deg) translateX(-60%);
          scale: (0.7);
        }
      }
    }
  }
}
</style>
