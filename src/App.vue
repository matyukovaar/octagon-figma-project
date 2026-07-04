<template>
  <div id="app">

    <!-- ========== ШАПКА ========== -->
    <header class="site-header">
      <div class="container header-content">
        <div class="logo">
          <span>KidsConnect</span>
        </div>
      </div>
    </header>

    <!-- ========== СТРАНИЦА: КАТАЛОГ ========== -->
    <div v-if="currentPage === 'catalog'" class="catalog-page">
      <div class="container">

        <!-- Панель управления -->
        <div class="toolbar">
          <div class="toolbar-left">
            <div class="search-box">
              <span class="search-icon">🔍</span>
              <input type="text" placeholder="Поиск" class="search-input" />
            </div>
            <div class="tabs">
              <button class="tab active">Все</button>
              <button class="tab">Платные</button>
              <button class="tab">Бесплатные</button>
            </div>
          </div>
          <button class="map-button">На карте 📍</button>
        </div>

        <div class="catalog-layout">

          <!-- Основной контент с карточками -->
          <main class="catalog-main">

            <!-- Категория: Силовой спорт -->
            <section class="category">
              <h2 class="category-title">Силовой спорт</h2>

              <!-- Карточка 1 -->
              <article class="card">
                <div class="card-image">
                  <img src="https://via.placeholder.com/200x150" alt="Тяжелая атлетика" />
                </div>
                <div class="card-content">
                  <div class="card-header">
                    <div class="card-title-section">
                      <h3 class="card-title">Тяжелая атлетика (в Юбилейном мкр.)</h3>
                      <span class="tag tag-free">Бесплатно</span>
                    </div>
                  </div>
                  <p class="card-tag">#Тяжелая атлетика</p>
                  <div class="card-info">
                    <p>👤 10-18 лет</p>
                    <p>🏢 г. Иркутск, Юбилейный мкр., стр. 49/1</p>
                    <p>📍 ФОК "Юбилейный"</p>
                  </div>
                  <div class="card-schedule">
                    <span class="schedule-days">🕒 Пн, Ср, Пт</span>
                    <span class="time-slot">09:00 - 10:30</span>
                    <span class="time-slot">12:00 - 13:30</span>
                    <span class="time-slot">18:00 - 19:30</span>
                  </div>
                </div>
                <button class="more-button" @click="openDetail('Тяжелая атлетика (в Юбилейном мкр.)')">
                  Подробнее
                </button>
              </article>

              <!-- Карточка 2 -->
              <article class="card">
                <div class="card-image">
                  <img src="https://via.placeholder.com/200x150" alt="Тяжелая атлетика" />
                </div>
                <div class="card-content">
                  <div class="card-header">
                    <div class="card-title-section">
                      <h3 class="card-title">Тяжелая атлетика (на ул. Боткина)</h3>
                      <div class="badges">
                        <span class="tag tag-first-free">Первое бесплатно</span>
                        <span class="tag tag-price">500 руб.</span>
                      </div>
                    </div>
                  </div>
                  <p class="card-tag">#Тяжелая атлетика</p>
                  <div class="card-info">
                    <p>👤 10-18 лет</p>
                    <p>🏢 г. Иркутск, Юбилейный мкр., стр. 49/1</p>
                    <p>📍 ФОК "Юбилейный"</p>
                  </div>
                  <div class="card-schedule">
                    <span class="schedule-days">🕒 Пн, Ср, Пт</span>
                    <span class="time-slot">09:00 - 10:30</span>
                    <span class="time-slot">12:00 - 13:30</span>
                  </div>
                </div>
                <button class="more-button" @click="openDetail('Тяжелая атлетика (на ул. Боткина)')">
                  Подробнее
                </button>
              </article>

              <!-- Карточка 3 -->
              <article class="card">
                <div class="card-image">
                  <img src="https://via.placeholder.com/200x150" alt="Тяжелая атлетика" />
                </div>
                <div class="card-content">
                  <div class="card-header">
                    <div class="card-title-section">
                      <h3 class="card-title">Тяжелая атлетика (на ул. Норильской)</h3>
                      <div class="badges">
                        <span class="tag tag-first-free">Первое бесплатно</span>
                        <span class="tag tag-price">3200 руб. в занятий</span>
                      </div>
                    </div>
                  </div>
                  <p class="card-tag">#Тяжелая атлетика</p>
                  <div class="card-info">
                    <p>👤 10-18 лет</p>
                    <p>🏢 г. Иркутск, Юбилейный мкр., стр. 49/1</p>
                    <p>📍 ФОК "Юбилейный"</p>
                  </div>
                  <div class="card-schedule">
                    <span class="schedule-days">🕒 Пн, Ср, Пт</span>
                    <span class="time-slot">09:00 - 10:30</span>
                    <span class="time-slot">12:00 - 13:30</span>
                    <span class="time-slot">18:00 - 19:30</span>
                  </div>
                </div>
                <button class="more-button" @click="openDetail('Тяжелая атлетика (на ул. Норильской)')">
                  Подробнее
                </button>
              </article>

              <!-- Карточка 4 -->
              <article class="card">
                <div class="card-image">
                  <img src="https://via.placeholder.com/200x150" alt="Пауэрлифтинг" />
                </div>
                <div class="card-content">
                  <div class="card-header">
                    <div class="card-title-section">
                      <h3 class="card-title">Пауэрлифтинг</h3>
                      <span class="tag tag-free">Бесплатно</span>
                    </div>
                  </div>
                  <p class="card-tag">#Пауэрлифтинг</p>
                  <div class="card-info">
                    <p>👤 10-18 лет</p>
                    <p>🏢 г. Иркутск, Юбилейный мкр., стр. 49/1</p>
                    <p>📍 ФОК "Юбилейный"</p>
                  </div>
                  <div class="card-schedule">
                    <span class="schedule-days">🕒 Пн, Ср, Пт</span>
                    <span class="time-slot">09:00 - 10:30</span>
                    <span class="time-slot">12:00 - 13:30</span>
                    <span class="time-slot">18:00 - 19:30</span>
                  </div>
                </div>
                <button class="more-button" @click="openDetail('Пауэрлифтинг')">
                  Подробнее
                </button>
              </article>
            </section>

            <!-- Категория: Единоборства -->
            <section class="category">
              <h2 class="category-title">Единоборства</h2>

              <article class="card">
                <div class="card-image">
                  <img src="https://via.placeholder.com/200x150" alt="Дзюдо" />
                </div>
                <div class="card-content">
                  <div class="card-header">
                    <div class="card-title-section">
                      <h3 class="card-title">Дзюдо</h3>
                      <span class="tag tag-free">Бесплатно</span>
                    </div>
                  </div>
                  <p class="card-tag">#Дзюдо</p>
                  <div class="card-info">
                    <p>👤 6-18 лет</p>
                    <p>🏢 г. Иркутск, ул. Трудовая, д.115А</p>
                    <p>📍 СК "Вымпел"</p>
                  </div>
                  <div class="card-schedule">
                    <span class="schedule-days">🕒 Пн, Ср, Пт</span>
                    <span class="time-slot">09:00 - 10:30</span>
                    <span class="time-slot">12:00 - 13:30</span>
                    <span class="time-slot">18:00 - 19:30</span>
                  </div>
                </div>
                <button class="more-button" @click="openDetail('Дзюдо')">
                  Подробнее
                </button>
              </article>

              <article class="card">
                <div class="card-image">
                  <img src="https://via.placeholder.com/200x150" alt="Вольная борьба" />
                </div>
                <div class="card-content">
                  <div class="card-header">
                    <div class="card-title-section">
                      <h3 class="card-title">Вольная борьба (на ул. Норильская)</h3>
                      <div class="badges">
                        <span class="tag tag-first-free">Первое бесплатно</span>
                        <span class="tag tag-price">3200 руб. месяц</span>
                      </div>
                    </div>
                  </div>
                  <p class="card-tag">#Дзюдо</p>
                  <div class="card-info">
                    <p>👤 6-18 лет</p>
                    <p>🏢 г. Иркутск, ул. Трудовая, д.115А</p>
                    <p>📍 СК "Вымпел"</p>
                  </div>
                  <div class="card-schedule">
                    <span class="schedule-days">🕒 Пн, Ср, Пт</span>
                    <span class="time-slot">09:00 - 10:30</span>
                    <span class="time-slot">12:00 - 13:30</span>
                    <span class="time-slot">18:00 - 19:30</span>
                  </div>
                </div>
                <button class="more-button" @click="openDetail('Вольная борьба')">
                  Подробнее
                </button>
              </article>
            </section>

            <!-- Категория: Единоборства (дополнительно) -->
            <section class="category">
              <h2 class="category-title">Единоборства</h2>

              <article class="card">
                <div class="card-image">
                  <img src="https://via.placeholder.com/200x150" alt="Дзюдо" />
                </div>
                <div class="card-content">
                  <div class="card-header">
                    <div class="card-title-section">
                      <h3 class="card-title">Дзюдо</h3>
                      <span class="tag tag-free">Бесплатно</span>
                    </div>
                  </div>
                  <p class="card-tag">#Дзюдо</p>
                  <div class="card-info">
                    <p>👤 6-18 лет</p>
                    <p>🏢 г. Иркутск, ул. Трудовая, д.115А</p>
                    <p>📍 СК "Вымпел"</p>
                  </div>
                  <div class="card-schedule">
                    <span class="schedule-days">🕒 Пн, Ср, Пт</span>
                    <span class="time-slot">09:00 - 10:30</span>
                    <span class="time-slot">12:00 - 13:30</span>
                    <span class="time-slot">18:00 - 19:30</span>
                  </div>
                </div>
                <button class="more-button" @click="openDetail('Дзюдо')">
                  Подробнее
                </button>
              </article>

              <article class="card">
                <div class="card-image">
                  <img src="https://via.placeholder.com/200x150" alt="Вольная борьба" />
                </div>
                <div class="card-content">
                  <div class="card-header">
                    <div class="card-title-section">
                      <h3 class="card-title">Вольная борьба (на ул. Норильская)</h3>
                      <div class="badges">
                        <span class="tag tag-first-free">Первое бесплатно</span>
                        <span class="tag tag-price">3200 руб. месяц</span>
                      </div>
                    </div>
                  </div>
                  <p class="card-tag">#Дзюдо</p>
                  <div class="card-info">
                    <p>👤 6-18 лет</p>
                    <p>🏢 г. Иркутск, ул. Трудовая, д.115А</p>
                    <p>📍 СК "Вымпел"</p>
                  </div>
                  <div class="card-schedule">
                    <span class="schedule-days">🕒 Пн, Ср, Пт</span>
                    <span class="time-slot">09:00 - 10:30</span>
                    <span class="time-slot">12:00 - 13:30</span>
                    <span class="time-slot">18:00 - 19:30</span>
                  </div>
                </div>
                <button class="more-button" @click="openDetail('Вольная борьба')">
                  Подробнее
                </button>
              </article>
            </section>

            <!-- Категория: Единоборства (еще) -->
            <section class="category">
              <h2 class="category-title">Единоборства</h2>

              <article class="card">
                <div class="card-image">
                  <img src="https://via.placeholder.com/200x150" alt="Дзюдо" />
                </div>
                <div class="card-content">
                  <div class="card-header">
                    <div class="card-title-section">
                      <h3 class="card-title">Дзюдо</h3>
                      <span class="tag tag-free">Бесплатно</span>
                    </div>
                  </div>
                  <p class="card-tag">#Дзюдо</p>
                  <div class="card-info">
                    <p>👤 6-18 лет</p>
                    <p>🏢 г. Иркутск, ул. Трудовая, д.115А</p>
                    <p>📍 СК "Вымпел"</p>
                  </div>
                  <div class="card-schedule">
                    <span class="schedule-days">🕒 Пн, Ср, Пт</span>
                    <span class="time-slot">09:00 - 10:30</span>
                    <span class="time-slot">12:00 - 13:30</span>
                    <span class="time-slot">18:00 - 19:30</span>
                  </div>
                </div>
                <button class="more-button" @click="openDetail('Дзюдо')">
                  Подробнее
                </button>
              </article>

              <article class="card">
                <div class="card-image">
                  <img src="https://via.placeholder.com/200x150" alt="Вольная борьба" />
                </div>
                <div class="card-content">
                  <div class="card-header">
                    <div class="card-title-section">
                      <h3 class="card-title">Вольная борьба (на ул. Норильская)</h3>
                      <div class="badges">
                        <span class="tag tag-first-free">Первое бесплатно</span>
                        <span class="tag tag-price">3200 руб. месяц</span>
                      </div>
                    </div>
                  </div>
                  <p class="card-tag">#Дзюдо</p>
                  <div class="card-info">
                    <p>👤 6-18 лет</p>
                    <p>🏢 г. Иркутск, ул. Трудовая, д.115А</p>
                    <p>📍 СК "Вымпел"</p>
                  </div>
                  <div class="card-schedule">
                    <span class="schedule-days">🕒 Пн, Ср, Пт</span>
                    <span class="time-slot">09:00 - 10:30</span>
                    <span class="time-slot">12:00 - 13:30</span>
                    <span class="time-slot">18:00 - 19:30</span>
                  </div>
                </div>
                <button class="more-button" @click="openDetail('Вольная борьба')">
                  Подробнее
                </button>
              </article>
            </section>

          </main>

          <!-- Боковая панель фильтров -->
          <aside class="filters-sidebar">
            <h2 class="filters-title">Фильтры</h2>

            <div class="filter-block">
              <label class="filter-label">Возраст</label>
              <select class="filter-select">
                <option>Любой</option>
                <option>3-5 лет</option>
                <option>6-8 лет</option>
                <option>9-12 лет</option>
                <option>13-16 лет</option>
              </select>
            </div>

            <div class="filter-block">
              <label class="filter-label">Пол</label>
              <div class="checkbox-group">
                <label class="checkbox-label">
                  <input type="checkbox" checked />
                  <span>Мужской</span>
                </label>
                <label class="checkbox-label">
                  <input type="checkbox" checked />
                  <span>Женский</span>
                </label>
              </div>
            </div>

            <div class="filter-block">
              <label class="filter-label">Каталог</label>

              <details open class="accordion">
                <summary class="accordion-header">Силовой спорт <span class="count">3</span></summary>
                <ul class="accordion-list">
                  <li>Тяжелая атлетика <span class="count">3</span></li>
                  <li>Пауэрлифтинг <span class="count">1</span></li>
                </ul>
              </details>

              <details open class="accordion">
                <summary class="accordion-header">Единоборства <span class="count">2</span></summary>
                <ul class="accordion-list">
                  <li>Вольная борьба <span class="count">1</span></li>
                  <li>Дзюдо <span class="count">1</span></li>
                </ul>
              </details>

              <details class="accordion">
                <summary class="accordion-header">ДПИ и ремесла</summary>
              </details>

              <details class="accordion">
                <summary class="accordion-header">Техническое конструирование</summary>
              </details>

              <details class="accordion">
                <summary class="accordion-header">Словесность</summary>
              </details>

              <details class="accordion">
                <summary class="accordion-header">Иностранные языки</summary>
              </details>

              <details class="accordion">
                <summary class="accordion-header">Развитие интеллекта</summary>
              </details>

              <details class="accordion">
                <summary class="accordion-header">Информационные технологии</summary>
              </details>

              <details class="accordion">
                <summary class="accordion-header">История и Традиции</summary>
              </details>

              <details class="accordion">
                <summary class="accordion-header">Педагогика</summary>
              </details>

              <details class="accordion">
                <summary class="accordion-header">Музыка и звук</summary>
              </details>

              <details class="accordion">
                <summary class="accordion-header">Пение</summary>
              </details>

              <details class="accordion">
                <summary class="accordion-header">Хореография(танцы)</summary>
              </details>

              <details class="accordion">
                <summary class="accordion-header">Зрелищные искусства</summary>
              </details>

              <details class="accordion">
                <summary class="accordion-header">Мода и стиль</summary>
              </details>

              <details class="accordion">
                <summary class="accordion-header">Познавательные развлечения</summary>
              </details>

              <details class="accordion">
                <summary class="accordion-header">Туризм</summary>
              </details>

              <details class="accordion">
                <summary class="accordion-header">Естественные науки</summary>
              </details>

              <details class="accordion">
                <summary class="accordion-header">Люди и животные</summary>
              </details>

              <details class="accordion">
                <summary class="accordion-header">Эстетические виды спорта</summary>
              </details>

              <details class="accordion">
                <summary class="accordion-header">Технические виды спорта</summary>
              </details>

              <details class="accordion">
                <summary class="accordion-header">Командно-игровой спорт</summary>
              </details>

              <details class="accordion">
                <summary class="accordion-header">Индивидуально игровой спорт</summary>
              </details>

              <details class="accordion">
                <summary class="accordion-header">Водные виды спорта</summary>
              </details>

              <details class="accordion">
                <summary class="accordion-header">Легкая атлетика и гимнастика</summary>
              </details>

              <details class="accordion">
                <summary class="accordion-header">Физкультура</summary>
              </details>
            </div>
          </aside>

        </div>
      </div>
    </div>

    <!-- ========== СТРАНИЦА: ДЕТАЛЬНАЯ ========== -->
    <div v-if="currentPage === 'detail'" class="detail-page">
      <div class="container">

        <!-- Кнопки навигации -->
        <div class="detail-toolbar">
          <button class="back-button" @click="currentPage = 'catalog'">← Назад</button>
          <button class="map-button">На карте 📍</button>
        </div>

        <article class="section-detail">

          <!-- Заголовок -->
          <h1 class="section-title">{{ selectedSection }}</h1>

          <!-- Верхний блок: картинка + инфо -->
          <div class="detail-header">
            <div class="detail-image">
              <img src="https://via.placeholder.com/300x200" alt="Секция" />
            </div>
            <div class="detail-info">
              <div class="detail-badges">
                <span class="tag tag-status">Набор открыт</span>
                <span class="tag tag-free">Бесплатно</span>
              </div>
              <div class="detail-meta">
                <p>👤 10-18 лет</p>
                <p>🏢 г. Иркутск, Юбилейный мкр., стр. 49/1</p>
                <p>📍 ФОК "Юбилейный"</p>
              </div>
              <button class="enroll-button">Записаться</button>
            </div>
          </div>

          <!-- Блок: Группы + Расписание -->
          <div class="detail-row">
            <div class="detail-block">
              <h2 class="block-title">ГРУППЫ</h2>
              <h3 class="block-subtitle">Этап начальной подготовки</h3>
              <div class="group-info">
                <p>👤 Петрова Елена Александровна</p>
                <p>👥 15 из 20</p>
                <p>📅 12 месяцев</p>
              </div>
            </div>

            <div class="detail-block">
              <h2 class="block-title">РАСПИСАНИЕ ЗАНЯТИЙ</h2>
              <div class="schedule-row">
                <span>🕒 Пн, Вт, Чт, Сб</span>
              </div>
              <div class="schedule-row">
                <span>🕒 Пн, Вт, Чт, Сб</span>
                <span class="time-slot">08:00 - 10:00</span>
                <span class="time-slot">18:00 - 19:30</span>
              </div>
            </div>
          </div>

          <!-- Блок: Описание -->
          <div class="detail-block full-width">
            <h2 class="block-title">ОПИСАНИЕ</h2>
            <p class="block-text">
              Лёгкая атлетика - олимпийский вид спорта, объединяющий беговые виды,
              спортивную ходьбу, технические виды (прыжки и метания), многоборья,
              пробеги (бег по шоссе), кроссы (бег по пересечённой местности).
            </p>
          </div>

          <!-- Блок: Содержание программы -->
          <div class="detail-block full-width">
            <h2 class="block-title">СОДЕРЖАНИЕ ПРОГРАММЫ</h2>

            <details open class="program-accordion">
              <summary class="accordion-header">Базовый уровень</summary>
              <div class="accordion-content">
                <h4>Базовый уровень</h4>
                <p>
                  Базовый уровень сложности первый-второй год обучения, 252 часа.
                </p>
                <ul class="program-list">
                  <li>Обязательные предметные области (количество часов - 15);</li>
                  <li>Вариативные предметные области (количество часов -10);</li>
                  <li>Теория (количество часов -5);</li>
                  <li>Практика (количество часов - 216);</li>
                  <li>Самостоятельная работа (количество часов -2);</li>
                  <li>Аттестация (количество часов - 4);</li>
                </ul>
                <p>
                  Базовый уровень сложности третий-четвертый год обучения, 416 часов.
                </p>
                <ul class="program-list">
                  <li>Обязательные предметные области (количество часов - 25);</li>
                  <li>Вариативные предметные области (количество часов - 15);</li>
                  <li>Теория (количество часов -7);</li>
                  <li>Практика (количество часов - 361);</li>
                  <li>Самостоятельная работа (количество часов - 4);</li>
                  <li>Аттестация (количество часов - 4);</li>
                </ul>
                <p>
                  Базовый уровень сложности пятый-шестой год обучения, 420 часов.
                </p>
                <ul class="program-list">
                  <li>Обязательные предметные области (количество часов - 27);</li>
                  <li>Вариативные предметные области (количество часов - 15);</li>
                  <li>Теория (количество часов - 8);</li>
                  <li>Практика (количество часов - 360);</li>
                  <li>Самостоятельная работа (количество часов - 6);</li>
                  <li>Аттестация (количество часов - 4);</li>
                </ul>
              </div>
            </details>

            <details class="program-accordion">
              <summary class="accordion-header">Углублённый уровень</summary>
              <div class="accordion-content">
                <p>Содержание углублённого уровня...</p>
              </div>
            </details>
          </div>

        </article>
      </div>
    </div>

  </div>
</template>

<script setup>
import { ref } from 'vue'

const currentPage = ref('catalog')
const selectedSection = ref('')

const openDetail = (sectionName) => {
  selectedSection.value = sectionName
  currentPage.value = 'detail'
}
</script>

<style>
/* ========== БАЗОВЫЕ СТИЛИ ========== */
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: -apple-system, BlinkMacSystemFont, 'Segoe UI', Roboto, 'Helvetica Neue', Arial, sans-serif;
  background: #F5F5F5;
  color: #333;
  line-height: 1.5;
}

.container {
  max-width: 1440px;
  margin: 0 auto;
  padding: 0 20px;
}

/* ========== ШАПКА ========== */
.site-header {
  background: #7C2D3A;
  padding: 20px 0;
  margin-bottom: 20px;
}

.header-content {
  display: flex;
  align-items: center;
}

.logo {
  display: flex;
  align-items: center;
  gap: 12px;
  color: white;
  font-size: 24px;
  font-weight: 600;
}

.logo img {
  width: 40px;
  height: 40px;
  border-radius: 8px;
}

/* ========== ПАНЕЛЬ УПРАВЛЕНИЯ ========== */
.toolbar {
  display: flex;
  justify-content: space-between;
  align-items: center;
  margin-bottom: 30px;
  gap: 20px;
}

.toolbar-left {
  display: flex;
  gap: 20px;
  align-items: center;
  flex: 1;
}

.search-box {
  display: flex;
  align-items: center;
  background: white;
  border: 1px solid #E0E0E0;
  border-radius: 8px;
  padding: 10px 16px;
  flex: 1;
  max-width: 300px;
}

.search-icon {
  margin-right: 8px;
}

.search-input {
  border: none;
  outline: none;
  font-size: 14px;
  width: 100%;
}

.tabs {
  display: flex;
  gap: 8px;
}

.tab {
  padding: 10px 20px;
  border: 1px solid #E0E0E0;
  background: white;
  border-radius: 8px;
  cursor: pointer;
  font-size: 14px;
  transition: all 0.2s;
}

.tab:hover {
  background: #F5F5F5;
}

.tab.active {
  background: #7C2D3A;
  color: white;
  border-color: #7C2D3A;
}

.map-button {
  padding: 10px 20px;
  background: white;
  border: 1px solid #E0E0E0;
  border-radius: 8px;
  cursor: pointer;
  font-size: 14px;
}

/* ========== КАТАЛОГ ========== */
.catalog-page {
  padding-bottom: 40px;
}

.catalog-layout {
  display: flex;
  gap: 20px;
}

.catalog-main {
  flex: 1;
}

/* ========== КАТЕГОРИИ ========== */
.category {
  margin-bottom: 40px;
}

.category-title {
  font-size: 24px;
  font-weight: 600;
  margin-bottom: 20px;
  color: #333;
}

/* ========== КАРТОЧКА ========== */
.card {
  background: white;
  border-radius: 12px;
  padding: 24px;
  margin-bottom: 20px;
  display: flex;
  gap: 24px;
  box-shadow: 0 2px 8px rgba(0,0,0,0.05);
}

.card-image img {
  width: 200px;
  height: 150px;
  object-fit: cover;
  border-radius: 8px;
}

.card-content {
  flex: 1;
}

.card-header {
  margin-bottom: 12px;
}

.card-title-section {
  display: flex;
  justify-content: space-between;
  align-items: flex-start;
  gap: 16px;
}

.card-title {
  font-size: 18px;
  font-weight: 600;
  color: #333;
  margin-bottom: 8px;
}

.badges {
  display: flex;
  gap: 8px;
  flex-shrink: 0;
}

.card-tag {
  color: #E97884;
  font-size: 14px;
  margin-bottom: 12px;
}

.card-info {
  margin-bottom: 12px;
}

.card-info p {
  font-size: 14px;
  color: #666;
  margin-bottom: 4px;
}

.card-schedule {
  display: flex;
  flex-wrap: wrap;
  gap: 12px;
  align-items: center;
}

.schedule-days {
  font-size: 14px;
  color: #666;
}

.time-slot {
  background: #F5E6C8;
  padding: 4px 12px;
  border-radius: 4px;
  font-size: 13px;
  color: #333;
}

.more-button {
  align-self: flex-start;
  padding: 12px 32px;
  background: #7C2D3A;
  color: white;
  border: none;
  border-radius: 8px;
  cursor: pointer;
  font-size: 14px;
  font-weight: 500;
  margin-left: auto;
  transition: background 0.2s;
}

.more-button:hover {
  background: #5a1f2a;
}

/* ========== ТЕГИ ========== */
.tag {
  display: inline-block;
  padding: 6px 12px;
  border-radius: 6px;
  font-size: 13px;
  font-weight: 500;
}

.tag-free {
  background: #E97884;
  color: white;
}

.tag-first-free {
  background: white;
  color: #7C2D3A;
  border: 1px solid #7C2D3A;
}

.tag-price {
  background: #E97884;
  color: white;
}

.tag-status {
  background: white;
  color: #7C2D3A;
  border: 1px solid #7C2D3A;
  margin-right: 12px;
}

/* ========== ФИЛЬТРЫ ========== */
.filters-sidebar {
  width: 350px;
  background: white;
  border-radius: 12px;
  padding: 24px;
  height: fit-content;
  box-shadow: 0 2px 8px rgba(0,0,0,0.05);
}

.filters-title {
  font-size: 20px;
  font-weight: 600;
  margin-bottom: 24px;
}

.filter-block {
  margin-bottom: 24px;
  padding-bottom: 24px;
  border-bottom: 1px solid #E0E0E0;
}

.filter-label {
  display: block;
  font-weight: 600;
  margin-bottom: 12px;
  font-size: 14px;
}

.filter-select {
  width: 100%;
  padding: 10px 12px;
  border: 1px solid #E0E0E0;
  border-radius: 8px;
  font-size: 14px;
  background: white;
}

.checkbox-group {
  display: flex;
  flex-direction: column;
  gap: 8px;
}

.checkbox-label {
  display: flex;
  align-items: center;
  gap: 8px;
  cursor: pointer;
  font-size: 14px;
}

.checkbox-label input[type="checkbox"] {
  width: 18px;
  height: 18px;
  cursor: pointer;
}

/* АККОРДЕОН */
.accordion {
  margin-bottom: 8px;
}

.accordion-header {
  padding: 10px 0;
  cursor: pointer;
  font-weight: 500;
  font-size: 14px;
  list-style: none;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.accordion-header::-webkit-details-marker {
  display: none;
}

.accordion-header::after {
  content: '▼';
  font-size: 12px;
  transition: transform 0.2s;
}

.accordion[open] .accordion-header::after {
  transform: rotate(180deg);
}

.accordion-list {
  list-style: none;
  padding-left: 16px;
  margin-top: 8px;
}

.accordion-list li {
  padding: 6px 0;
  font-size: 14px;
  color: #666;
  display: flex;
  justify-content: space-between;
}

.count {
  color: #999;
  font-size: 13px;
}

/* ========== ДЕТАЛЬНАЯ СТРАНИЦА ========== */
.detail-page {
  padding-bottom: 40px;
}

.detail-toolbar {
  display: flex;
  justify-content: space-between;
  margin-bottom: 24px;
}

.back-button {
  padding: 10px 20px;
  background: white;
  border: 1px solid #E0E0E0;
  border-radius: 8px;
  cursor: pointer;
  font-size: 14px;
}

.section-detail {
  background: white;
  border-radius: 12px;
  padding: 32px;
  box-shadow: 0 2px 8px rgba(0,0,0,0.05);
}

.section-title {
  font-size: 28px;
  font-weight: 600;
  margin-bottom: 24px;
  color: #333;
}

.detail-header {
  display: flex;
  gap: 32px;
  margin-bottom: 32px;
  padding-bottom: 32px;
  border-bottom: 2px solid #E0E0E0;
}

.detail-image img {
  width: 300px;
  height: 200px;
  object-fit: cover;
  border-radius: 8px;
}

.detail-info {
  flex: 1;
}

.detail-badges {
  margin-bottom: 16px;
}

.detail-meta {
  margin-bottom: 24px;
}

.detail-meta p {
  margin-bottom: 8px;
  font-size: 14px;
  color: #666;
}

.enroll-button {
  padding: 16px 48px;
  background: #7C2D3A;
  color: white;
  border: none;
  border-radius: 8px;
  cursor: pointer;
  font-size: 16px;
  font-weight: 500;
}

.enroll-button:hover {
  background: #5a1f2a;
}

.detail-row {
  display: flex;
  gap: 32px;
  margin-bottom: 32px;
  padding-bottom: 32px;
  border-bottom: 2px solid #E0E0E0;
}

.detail-block {
  flex: 1;
}

.detail-block.full-width {
  width: 100%;
}

.block-title {
  font-size: 16px;
  font-weight: 600;
  margin-bottom: 16px;
  color: #333;
  text-transform: uppercase;
}

.block-subtitle {
  font-size: 16px;
  font-weight: 600;
  margin-bottom: 12px;
  color: #333;
}

.group-info p {
  margin-bottom: 8px;
  font-size: 14px;
  color: #666;
}

.schedule-row {
  display: flex;
  align-items: center;
  gap: 12px;
  margin-bottom: 8px;
}

.block-text {
  font-size: 14px;
  line-height: 1.6;
  color: #666;
}

/* АККОРДЕОН ПРОГРАММЫ */
.program-accordion {
  margin-bottom: 16px;
  border: 1px solid #E0E0E0;
  border-radius: 8px;
}

.program-accordion > summary {
  padding: 16px;
  cursor: pointer;
  font-weight: 600;
  background: #FAFAFA;
  border-radius: 8px;
  list-style: none;
  display: flex;
  justify-content: space-between;
  align-items: center;
}

.program-accordion > summary::-webkit-details-marker {
  display: none;
}

.program-accordion > summary::after {
  content: '▲';
  font-size: 12px;
}

.program-accordion:not([open]) > summary::after {
  content: '▼';
}

.accordion-content {
  padding: 20px;
}

.accordion-content h4 {
  margin-bottom: 12px;
  color: #333;
}

.accordion-content p {
  font-size: 14px;
  color: #666;
  margin-bottom: 12px;
}

.program-list {
  list-style: none;
  padding-left: 0;
}

.program-list li {
  padding: 4px 0;
  font-size: 14px;
  color: #666;
  padding-left: 16px;
  position: relative;
}

.program-list li::before {
  content: '•';
  position: absolute;
  left: 0;
  color: #7C2D3A;
}
</style>