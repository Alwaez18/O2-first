<script setup>
import { ref } from 'vue';
import HeaderBottom from '../components/header/header-bottom.vue';
import HeaderMain from '../components/header/header-main.vue';
import HeaderTop from '../components/header/header-top.vue';
import HeroSectionAction from '../components/hero-section/hero-section-action.vue';
import HeroSectionBlocks from '../components/hero-section/hero-section-blocks.vue';
import HeroSectionCard from '../components/hero-section/hero-section-card.vue';
import MainHeader from '../components/main/main-header.vue';
import MainSearch from '../components/main/main-search.vue';
import MainNew from '../components/main/main-new.vue';
import FooterTop from '../components/footer/footerTop.vue';
import FooterBotomn from '../components/footer/footerBotomn.vue';



const booksCard = ref([
  {
    image: "/img/book1.png", // Просто путь от корня, так как файлы в public
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

const MainKriterys = ref([
    {
        image:"/img/oklock.png",
        titleText:"Быстрая доставка",
        Text:"Доставим бесплатно от 2000 ₽ по всей России"
    },
    {
        image:"/img/oklock.png",
        titleText:"Быстрая доставка",
        Text:"Доставим бесплатно от 2000 ₽ по всей России"
    },
    {
        image:"/img/oklock.png",
        titleText:"Быстрая доставка",
        Text:"Доставим бесплатно от 2000 ₽ по всей России"
    },
    {
        image:"/img/oklock.png",
        titleText:"Быстрая доставка",
        Text:"Доставим бесплатно от 2000 ₽ по всей России"
    },
    {
        image:"/img/oklock.png",
        titleText:"Быстрая доставка",
        Text:"Доставим бесплатно от 2000 ₽ по всей России"
    },
]);
const mainNews = ref([
    {
    image:"/img/news.png",
    TitleText:"Бесплатный онлайн-семинар. Доктрина stare decisis: борьба за прецедент в рос...",
    Date:"16 июня 2020",
    Text:"18 июня в «Клубе цивилистов» пройдет бесплатный онлайн-семинар по проблематике судебного прецедента. Мероприятие приуроч...",
    },
    {
    image:"/img/news.png",
    TitleText:"Бесплатный онлайн-семинар. Доктрина stare decisis: борьба за прецедент в рос...",
    Date:"16 июня 2020",
    Text:"18 июня в «Клубе цивилистов» пройдет бесплатный онлайн-семинар по проблематике судебного прецедента. Мероприятие приуроч...",
    },
    {
    image:"/img/news.png",
    TitleText:"Бесплатный онлайн-семинар. Доктрина stare decisis: борьба за прецедент в рос...",
    Date:"16 июня 2020",
    Text:"18 июня в «Клубе цивилистов» пройдет бесплатный онлайн-семинар по проблематике судебного прецедента. Мероприятие приуроч...",
    },
]);
</script>





<template>
    <header class="header">
       <div>
        <HeaderTop

        />
       </div>
       <div>
        <HeaderMain

        />
       </div>
       <div>
        <HeaderBottom
        />
       </div>

    </header>

    <main class="main">
        <section class="hero-section">
            <div class="container">
                <div class="hero-section__grid">
                    <!-- Зелёный блок (2=3) -->
                     <HeroSectionAction
                     />
                        <HeroSectionBlocks
                        />
                            <HeroSectionCard
                            title="Акция дня"
                             image="/img/book day.png"
                             bookTitle="Другая книга"
                             author="Иванов И.И."
                             price="3200"
                            />
                </div>
            </div>
        </section>
        <div class="container">
            <MainHeader
            titleText="Новые Поступления"
            />
        </div>
        <section class="main">
            <div class="container">
                <div class="main-info">
    <!-- Карточка 1 -->
                  <BookCard
                    imageSrc="/img/book.png"
                    title="Инвестирование: способы, риски, субъекты : монография"
                    author="Майфат А.В."
                    category="Корпоративное право"
                    :formattedPrice="4450"
                    :rating="4.9"
                    :recommendation="89"
                    :badges="[
                      { text: 'Бесцеллер', type: 'default' },
                      { text: '1+1=3', type: 'red' }
                    ]"
                  />

                  <!-- Карточка 2 (мобильная версия) -->
                  <BookCard
                    imageSrc="/img/book1.png"
                    title="Инвестирование: способы, риски, субъекты : монография"
                    author="Майфат А.В."
                    category="Корпоративное право"
                    :formatedprice="4450"
                    :rating="4.9"
                    :recommendation="89"
                    :badges="[
                      { text: 'Новинка', type: 'green' }
                    ]"
                    :isMobile="true"
                  />

                  <!-- Карточка 3 (со скидкой) -->
                  <BookCard
                    imageSrc="/img/book2.png"
                    title="Инвестирование: способы, риски, субъекты : монография"
                    author="Майфат А.В."
                    category="Корпоративное право"
                    :formattedPrice="984"
                    :originalPrice="1284"
                    :rating="4.9"
                    :recommendation="89"
                  />
                  <BookCard
                    imageSrc="/img/book2.png"
                    title="Инвестирование: способы, риски, субъекты : монография"
                    author="Майфат А.В."
                    category="Корпоративное право"
                    :formattedPrice="984"
                    :originalPrice="1284"
                    :rating="4.9"
                    :recommendation="89"
                  />
                </div>



                <div>
                    <MainSearch
                    />
                </div>

            </div>
        </section>
            <div class="container">
                <MainHeader
            titleText="Готовяться к выходу"
            />
            </div>

        <section class="main">
            <div class="container">
                <div class="main-info">

                  <BookCard
                    imageSrc="/img/book.png"
                    title="Инвестирование: способы, риски, субъекты : монография"
                    author="Майфат А.В."
                    category="Корпоративное право"
                    :formattedPrice="4450"
                    :rating="4.9"
                    :recommendation="89"
                    :badges="[
                      { text: 'Бесцеллер', type: 'default' },
                      { text: '1+1=3', type: 'red' }
                    ]"
                  />

                  <!-- Карточка 2 (мобильная версия) -->
                  <BookCard
                    imageSrc="/img/book1.png"
                    title="Инвестирование: способы, риски, субъекты : монография"
                    author="Майфат А.В."
                    category="Корпоративное право"
                    :formatedprice="4450"
                    :rating="4.9"
                    :recommendation="89"
                    :badges="[
                      { text: 'Новинка', type: 'green' }
                    ]"
                    :isMobile="true"
                  />

                  <!-- Карточка 3 (со скидкой) -->
                  <BookCard
                    imageSrc="/img/book2.png"
                    title="Инвестирование: способы, риски, субъекты : монография"
                    author="Майфат А.В."
                    category="Корпоративное право"
                    :formattedPrice="984"
                    :originalPrice="1284"
                    :rating="4.9"
                    :recommendation="89"
                    :badges="[
                        { text: 'Бесцеллер', type: 'default' },
                        { text: '1+1=3', type: 'red' }
                    ]"
                  />
                  <BookCard
                    imageSrc="/img/book2.png"
                    title="Инвестирование: способы, риски, субъекты : монография"
                    author="Майфат А.В."
                    category="Корпоративное право"
                    :formattedPrice="984"
                    :originalPrice="1284"
                    :rating="4.9"
                    :recommendation="89"
                    :badges="[
                        { text: 'Бесцеллер', type: 'default' },
                        { text: '1+1=3', type: 'red' }
                    ]"

                  />
                </div>
                <div class="main-info__all-books">
                    <a href="" class="main-info__link">Показать все книги раздела</a>
                </div>
                <div class="main-kritery">
                    <MainKritery
                    v-for="(item, index) in MainKriterys"
                    :key="index"
                    :image="item.image.default"
                    :titleText="item.titleText"
                    :Text="item.Text"
                    />
                </div>
                    <MainHeader
                        titleText="Новости"
                    />

                <div class="main-news">
                    <MainNew
                    v-for="(item, index) in mainNews"
                    :key="index"
                    :image="item.image"
                    :Date="item.Date"
                    :TitleText="item.TitleText"
                    :Text="item.Text"
                    />

                </div>
            </div>
        </section>
    </main>
    <FooterTop
    />

    <footer class="footer">
        <div class="container">
            <!-- Основное меню футера -->
          <div>
                  <!-- Другие компоненты -->
                  <Footer />
          </div>

          <div>
            <FooterBotomn
            />
            </div>
        </div>
      </footer>
</template>
