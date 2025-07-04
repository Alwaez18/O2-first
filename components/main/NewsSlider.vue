<template>
    <div class="news-swiper">
      <swiper
        :modules="modules"
        :slides-per-view="slidesPerView"
        :space-between="30"
        navigation
      >
        <swiper-slide v-for="(news, index) in newsList" :key="index">
          <MainNews
            :image="news.image"
            :Date="news.Date"
            :TitleText="news.TitleText"
            :Text="news.Text"
            :index="index"
          />
        </swiper-slide>
      </swiper>
    </div>
  </template>

  <script setup>
  import { ref, onMounted, onUnmounted } from 'vue';
  import { Navigation } from 'swiper/modules';
  import 'swiper/css';
  import 'swiper/css/navigation';
  import MainNews from './MainNews.vue';
  import { Swiper, SwiperSlide } from 'swiper/vue';

  const props = defineProps({
    newsList: {
      type: Array,
      required: true
    }
  });

  const modules = [Navigation];
  const slidesPerView = ref(4);

  const updateSlides = () => {
    slidesPerView.value = window.innerWidth < 375 ? 1 : 1;
  };

  onMounted(() => {
    updateSlides();
    window.addEventListener('resize', updateSlides);
  });

  onUnmounted(() => {
    window.removeEventListener('resize', updateSlides);
  });
  </script>

<style lang="scss">
.news-swiper {
  padding: 20px;
  max-width: 1200px;
  margin: 0 auto;

  .swiper {
    width: 100%;
    padding: 10px 0; // Добавляем отступы сверху и снизу
  }

  .swiper-slide {
    display: flex;
    justify-content: center;
    height: auto; // Важно для правильной высоты
  }

  // Стили для десктопа
  .swiper-slide {
    width: calc(25% - 20px); // 4 карточки с отступами
    min-width: 250px; // Минимальная ширина карточки
  }

  // Стили для навигационных кнопок
  .swiper-button-next,
  .swiper-button-prev {
    color: #333;
    background: white;
    border-radius: 50%;
    width: 40px;
    height: 40px;
    box-shadow: 0 2px 8px rgba(0,0,0,0.15);
    &::after {
      font-size: 18px;
      font-weight: bold;
    }
  }

  @media (max-width: 375px) {
    padding: 15px 10px;
    max-width: 100%;

    .swiper {
      max-width: 100%;
      padding: 0 30px; // Добавляем пространство для свайпа
    }

    .swiper-slide {
      width: 100% !important; // На мобильных 1 карточка на весь экран
      padding: 0 5px; // Небольшие отступы по бокам
    }

    // Скрываем кнопки навигации на мобильных
    .swiper-button-next,
    .swiper-button-prev {
      display: none;
    }

    // Стили для индикаторов (если добавите pagination)
    .swiper-pagination {
      position: relative;
      margin-top: 15px;

      .swiper-pagination-bullet {
        width: 8px;
        height: 8px;
        background: #ccc;
        opacity: 1;

        &-active {
          background: #333;
        }
      }
    }
  }
}

// Дополнительные стили для карточек
.main-news__block {
  width: 100%;
  height: 100%;
  display: flex;
  flex-direction: column;
}
</style>