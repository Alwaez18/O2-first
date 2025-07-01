<script setup>

const booksCard = ref([
  {
    image: "/img/book.png",
    title: "Инвестирование: способы, риски, субъекты : монография",
    author: "Майфат А.В.",
    category: "Корпоративное право",
    price: 4450,
    isBestseller: true,
    promoBadge: "1+1=3",
    rating: 4.9,
    recommendation: 89
  },
  {
    image: "/img/book1.png",
    title: "Другая книга",
    author: "Иванов И.И.",
    category: "Гражданское право",
    price: 3200,
    isBestseller: false,
    promoBadge: "Скидка 20%",
    rating: 4.7,
    recommendation: 92
  },
  {
    image: "/img/book1.png",
    title: "Другая книга",
    author: "Иванов И.И.",
    category: "Гражданское право",
    price: 3200,
    isBestseller: false,
    promoBadge: "Скидка 20%",
    rating: 4.7,
    recommendation: 92
  },
  {
    image: "/img/book1.png",
    title: "Другая книга",
    author: "Иванов И.И.",
    category: "Гражданское право",
    price: 3200,
    isBestseller: false,
    promoBadge: "Скидка 20%",
    rating: 4.7,
    recommendation: 92
  },
  // ... остальные книги
]);
</script>




<template>
    <header class="header">
        <section class="header__up">
            <div class="container">
                <div class="header-up">
                    <nav class="header-up__left">
                        <div class="header-up__left-link">
                            <img loading="lazy" src="../img/location.svg" alt="">
                            <a href="">Москва</a>
                        </div>
                        <div class="header-up__left-link">
                            <img src="../img/dostavka.svg" alt="">
                            <a href="">Доставка и оплата</a>
                        </div>
                        <div class="header-up__left-link">
                            <img src="../img/adress.svg" alt="">
                            <a href="">Адрес и часы работы</a>
                        </div>
                    </nav>
                    <nav class="header-up__right">
                        <div class="header-up__right-link">
                            <img src="../img/email.svg" alt="">
                            <a href="">market@estatut.ru</a>
                        </div>
                        <div class="header-up__right-link">
                            <img src="../img/phone.svg" alt="">
                            <a href="">8 (968) 660-65-50</a>
                            <img src="../img/green.svg" alt="">
                        </div>
                    </nav>
                </div>
            </div>
        </section>
        <div class="line"></div>
        <section class="header-main">  <!-- Блок -->
            <div class="container">
              <div class="header-main__content">  <!-- Элемент -->
                <div class="header-main__search">  <!-- Элемент -->
                    <img src="/public/img/katalog.svg" alt="" class="header-main__mobile">
                  <img src="/public/img/logo (2).svg" alt="Логотип" class="header-main__logo">
                  <div class="header-main__search-wrapper">
                    <input type="search" class="header-main__search-input" placeholder="Что будем искать?" src="../img/search.svg">
                    <button class="header-main__search-button">
                      <img src="/public/img/search.svg" alt="Поиск" class="header-main__search-icon">
                      <span class="header-main__search-text">Искать</span>
                    </button>
                    <img src="/public/img/korzina.svg" alt="" class="header-main__mobile">
                  </div>
                </div>

                <nav class="header-main__nav">  <!-- Элемент -->
                  <div class="header-main__nav-item">  <!-- Элемент -->
                    <img src="/public/img/otlozheno.svg" alt="Отложено" class="header-main__nav-icon">
                    <a href="#" class="header-main__nav-link">Отложено</a>
                  </div>
                  <div class="header-main__nav-item">
                    <img src="/public/img/login.svg" alt="Войти" class="header-main__nav-icon">
                    <a href="#" class="header-main__nav-link">Войти</a>
                  </div>
                  <div class="header-main__nav-item">
                    <img src="/public/img/korzina.svg" alt="Корзина" class="header-main__nav-icon">
                    <a href="#" class="header-main__nav-link">Корзина</a>
                     <!-- Элемент -->
                  </div>
                </nav>
              </div>
            </div>
          </section>

          <section class="header-bottom">
            <div class="container">
                <div class="header-bottom__content">
                    <nav class="header-bottom__nav">
                        <div class="header-bottom__nav-item">
                            <img src="/public/img/katalog.svg" alt="" class="header-bottom__nav-img">
                            <a href="" class="header-bottom__nav-link">Каталог</a>
                        </div>
                        <div class="header-bottom__nav-item">
                            <a href="" class="header-bottom__nav-link">Авторы</a>
                        </div>
                        <div class="header-bottom__nav-item">
                            <a href="" class="header-bottom__nav-link">Новинки</a>
                        </div>
                        <div class="header-bottom__nav-item">
                            <img src="/public/img/sale.svg" alt="" class="header-bottom__nav-img">
                            <a href="" class="header-bottom__nav-link header-bottom__nav-link--orange">Скидки</a>
                        </div>
                        <div class="header-bottom__nav-item">

                            <a href="" class="header-bottom__nav-link">Партнёрам</a>
                        </div>
                        <div class="header-bottom__nav-item">

                            <a href="" class="header-bottom__nav-link">Мы</a>
                        </div>
                    </nav>
                </div>
            </div>
          </section>
    </header>

    <main class="main">
        <section class="hero-section">
            <div class="container">
                <div class="hero-section__grid">
                    <!-- Зелёный блок (2=3) -->
                    <div class="hero-section__action">
                        <div class="">
                            <button class="hero-section__button"><img loading="lazy" src="/public/img/arrow-left.svg" alt=""></button>
                        </div>
                        <button class="hero-section__button"><img loading="lazy" src="/public/img/arrow-right.svg" alt=""></button>
                        <div class="">
                        </div>
                    </div>

                    <!-- Фиолетовый и розовый блоки -->
                    <div class="hero-section__blocks">
                        <div class="hero-section__block hero-section__block--purple">
                            <p class="hero-section__text">
                                 доставим
                                ваш заказ при
                                покупке от 2000 ₽
                            </p>
                            <img loading="lazy" src="/public/img/purple-block.svg" alt="">
                        </div>
                        <div class="hero-section__block hero-section__block--pink">
                            <p class="hero-section__text--registr">
                                Скидка
                                при регистрации
                                до
                            </p>
                                <img loading="lazy" src="/public/img/pink.svg" alt="">
                        </div>
                    </div>

                    <!-- Карточка товара (справа, на всю высоту) -->
                    <article class="hero-section__product-card">
                        <div class="hero-section__product-card__up">
                            <h3 class="hero-section__product-card__title">Книга дня</h3>
                        <time datetime="2025-06-18TH08:56:31" class="hero-section__product-card__time">08:56:31</time>
                        </div>
                        <div class="hero-section__product-card__main">
                            <img loading="lazy" src="../img/book day.png" alt="" class="hero-section__product-card__img">
                        </div>
                        <div class="hero-section__product-card__low">
                            <span class="hero-section__product-card__desription">Корпоративное право</span>
                            <span class="hero-section__product-card__desription hero-section__product-card__desription--black">Инвестирование: способы, риски, субъекты : монография</span>
                            <span class="hero-section__product-card__desription">Майфат А.В.</span>
                            <span class="hero-section__product-card__desription hero-section__product-card__desription--sale">4 450 ₽ </span>
                        </div>
                        <div class="hero-section__product-card__buttons">
                            <button class="hero-section__product-card__button"> Корзина <img src="../img/basket.svg" alt=""> </button>
                            <button class="hero-section__product-card__button hero-section__product-card__button--"><img src="../img/favorite.svg" alt=""></button>
                        </div>
                    </article>
                </div>
            </div>
        </section>
        <section class="main-header">
            <div class="container">
                <div class="main-content">
                    <div class="main-content__header">
                        <h1 class="main-content__title">Новые поступления</h1>
                        <nav class="main-content-nav">
                            <button class="main-content-nav__button">> </button>
                            <button class="main-content-nav__button main-content-nav__button--rotate">></button>
                        </nav>
                    </div>
                </div>
            </div>
        </section>
        <section class="main">
            <div class="container">

                <div class="main-info">
                    <BookCard
                        v-for="(item, index) in booksCard"
                        :key="index"
                        :image="item.image"
                        :title="item.title"
                        :author="item.author"
                        :price="item.price"
                        :category="item.category"
                        :is-bestseller="item.isBestseller"
                        :promo-badge="item.promoBadge"
                        :rating="item.rating"
                        :recommendation="item.recommendation"
                    />
                </div>

                <div class="main-info__all-books">
                    <a href="" class="main-info__link">Показать все книги раздела</a>
                </div>
                <div class="main-search">
                   <div class="main-searh__flex">
                        <h3 class="main-search__title">Скидка</h3> <h3 class="main-search__text">при подписке на рассылку Издательства</h3>
                   </div>
                        <input type="email" class="main-search__input" placeholder="Введите ваш Email">
                        <button class="main-search__button">Подписаться</button>
                </div>
            </div>
        </section>
        <section class="main-header">
            <div class="container">
                <div class="main-content">
                    <div class="main-content__header">
                        <h2 class="main-content__title">Готовяться к выходу</h2>
                        <nav class="main-content-nav">
                            <button class="main-content-nav__button">> </button>
                            <button class="main-content-nav__button main-content-nav__button--rotate">></button>
                        </nav>
                    </div>
                </div>
            </div>
        </section>
        <section class="main">
            <div class="container">
                <div class="main-info">
                    <BookCard
                    v-for="(item, index) in booksCard"
                    :key="index"
                    :image="item.image"
                    :title="item.title.default"
                    :author="item.author.default"
                    :price="item.price.default"
                    :category="item.category.default"
                    :is-bestseller="item.isBestseller.default"
                    :promo-badge="item.promoBadge.default"
                    :rating="item.rating.default"
                    :recommendation="item.recommendation.default"
                    />
                </div>
                <div class="main-info__all-books">
                    <a href="" class="main-info__link">Показать все книги раздела</a>
                </div>
                <div class="main-kritery">
                    <article class="main-kritery__block">
                        <div class="main-kritery__left">
                            <img loading="lazy" src="../img/oklock.png" alt="" class="main-kritery__img">
                        </div>
                        <div class="main-kritery__right">
                            <h4 class="main-kritery__title">Быстрая доставка</h4>
                            <p class="main-kritery__text">Доставим бесплатно
                                                        от 2000 ₽ по всей России</p>
                        </div>
                    </article>
                    <article class="main-kritery__block">
                        <div class="main-kritery__left">
                            <img loading="lazy" src="../img/oklock.png" alt="" class="main-kritery__img">
                        </div>
                        <div class="main-kritery__right">
                            <h4 class="main-kritery__title">Быстрая доставка</h4>
                            <p class="main-kritery__text">Доставим бесплатно
                                                        от 2000 ₽ по всей России</p>
                        </div>
                    </article>
                    <article class="main-kritery__block">
                        <div class="main-kritery__left">
                            <img loading="lazy" src="../img/oklock.png" alt="" class="main-kritery__img">
                        </div>
                        <div class="main-kritery__right">
                            <h4 class="main-kritery__title">Быстрая доставка</h4>
                            <p class="main-kritery__text">Доставим бесплатно
                                                        от 2000 ₽ по всей России</p>
                        </div>
                    </article>
                    <article class="main-kritery__block">
                        <div class="main-kritery__left">
                            <img loading="lazy" src="../img/oklock.png" alt="" class="main-kritery__img">
                        </div>
                        <div class="main-kritery__right">
                            <h4 class="main-kritery__title">Быстрая доставка</h4>
                            <p class="main-kritery__text">Доставим бесплатно
                                                        от 2000 ₽ по всей России</p>
                        </div>
                    </article>
                </div>
                <div class="main-content__header">
                    <h2 class="main-content__title">Новости</h2>
                    <nav class="main-content-nav">
                        <button class="main-content-nav__button">> </button>
                        <button class="main-content-nav__button main-content-nav__button--rotate">></button>
                    </nav>
                </div>
                <div class="main-news">
                    <article class="main-news__block">
                        <div class="main-news__up">
                            <img loading="lazy" src="../img/news.png" alt="" class="main-news__img">
                        </div>
                        <div class="main-news__info">
                            <span class="main-news__date">16 июня 2020</span>
                            <h3 class="main-news__title">Бесплатный онлайн-семинар. Доктрина stare decisis: борьба за прецедент в рос...</h3>
                            <p class="main-news__text">18 июня в «Клубе цивилистов» пройдет
                                                        бесплатный онлайн-семинар по проблематике
                                                        судебного прецедента. Мероприятие приуроч...</p>
                            <button class="main-news__button">Читать</button>
                        </div>
                    </article>
                    <article class="main-news__block main-news__block--empty">
                        <div class="main-news__up">
                            <img loading="lazy" src="../img/news.png" alt="" class="main-news__img">
                        </div>
                        <div class="main-news__info">
                            <span class="main-news__date">16 июня 2020</span>
                            <h3 class="main-news__title">Бесплатный онлайн-семинар. Доктрина stare decisis: борьба за прецедент в рос...</h3>
                            <p class="main-news__text">18 июня в «Клубе цивилистов» пройдет
                                                        бесплатный онлайн-семинар по проблематике
                                                        судебного прецедента. Мероприятие приуроч...</p>
                            <button class="main-news__button">Читать</button>
                        </div>
                    </article>
                    <article class="main-news__block main-news__block--empty">
                        <div class="main-news__up">
                            <img loading="lazy" src="../img/news.png" alt="" class="main-news__img">
                        </div>
                        <div class="main-news__info">
                            <span class="main-news__date">16 июня 2020</span>
                            <h3 class="main-news__title">Бесплатный онлайн-семинар. Доктрина stare decisis: борьба за прецедент в рос...</h3>
                            <p class="main-news__text">18 июня в «Клубе цивилистов» пройдет
                                                        бесплатный онлайн-семинар по проблематике
                                                        судебного прецедента. Мероприятие приуроч...</p>
                            <button class="main-news__button">Читать</button>
                        </div>
                    </article>
                </div>
            </div>
        </section>
    </main>

    <div class="footer__top">
        <div class="container">
            <div class="footer__subscribe">
                <img src="../img/logo (2).svg" alt="">
                <form class="footer__form">
                  <input type="email" class="footer__input" placeholder="Введите свой Email и получите скидку">
                  <button type="submit" class="footer__button"><img src="../img/Send r_15.svg" alt=""></button>
                </form>
                <div class="footer__networks">
                  <img src="../img/Twitter Copy 3.svg" alt="">
                  <img src="../img/Twitter Copy 3.svg" alt="">
                  <img src="../img/Twitter Copy 3.svg" alt="">
                </div>
              </div>
        </div>

      </div>

    <footer class="footer">
        <div class="container">
            <!-- Основное меню футера -->
          <div class="footer__main">
            <div class="footer__column ">
              <h4 class="footer__column-title ">Покупателям</h4>
              <img src="../img/strelka.svg" alt="" class="footer__column-empty">
              <ul class="footer__list">
                <li class="footer__item"><a href="#" class="footer__link">Наша почта</a></li>
                <li class="footer__item"><a href="#" class="footer__link">Оплата и доставка</a></li>
                <li class="footer__item"><a href="#" class="footer__link">Вопросы и ответы</a></li>
                <li class="footer__item"><a href="#" class="footer__link">Контакты</a></li>
              </ul>
            </div>

            <div class="footer__column">
              <h4 class="footer__column-title">Издательство</h4>
              <img src="../img/strelka.svg" alt="" class="footer__column-empty">
              <ul class="footer__list">
                <li class="footer__item"><a href="#" class="footer__link">О компании</a></li>
                <li class="footer__item"><a href="#" class="footer__link">Авторам</a></li>
                <li class="footer__item"><a href="#" class="footer__link">Вакансии</a></li>
              </ul>
            </div>

            <div class="footer__column">
              <h4 class="footer__column-title">Книги</h4>
              <img src="../img/strelka.svg" alt="" class="footer__column-empty">
              <ul class="footer__list">
                <li class="footer__item"><a href="#" class="footer__link">Все категории</a></li>
                <li class="footer__item"><a href="#" class="footer__link">Бестселлеры</a></li>
                <li class="footer__item"><a href="#" class="footer__link">Новинки</a></li>
                <li class="footer__item"><a href="#" class="footer__link">Скидки и акции</a></li>
              </ul>
            </div>

            <div class="footer__column">
              <h4 class="footer__column-title">Прайс-лист</h4>
              <img src="../img/strelka.svg" alt="" class="footer__column-empty">
              <ul class="footer__list">
                <li class="footer__item"><a href="#" class="footer__link">Скачать прайс-лист</a></li>
                <li class="footer__item"><a href="#" class="footer__link">PDF, 12 Мb</a></li>
              </ul>
            </div>

            <div class="footer__column">
              <h4 class="footer__column-title">Телефон и Email</h4>
              <img src="../img/strelka.svg" alt="" class="footer__column-empty">
              <ul class="footer__list">
                <li class="footer__item"><a href="mailto:market@estatut.ru" class="footer__link">market@estatut.ru</a></li>
                <li class="footer__item"><a href="tel:89686606550" class="footer__link">8 (968) 660-65-50</a></li>
              </ul>
            </div>
          </div>

          <!-- Нижняя часть футера -->
          <div class="footer__bottom">
            <div class="footer__copyright">© 2020 Издательство «Статут»</div>
            <div class="footer__address">ул. Лобачевского, 92, корп. 2 119454, г. Москва</div>
            <div class="footer__legal">
              <a href="#" class="footer__legal-link">Политика конфиденциальности</a>
              <a href="#" class="footer__legal-link">Договор оферты</a>
            </div>
          </div>
        </div>
      </footer>
</template>
<script setup>
</script>
