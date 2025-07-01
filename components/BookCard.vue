<template>
    <article class="main-info__card">
      <img
        loading="lazy"
        :src="getImageUrl('/img/book1.png')"
        :alt="title"
        class="main-info__book"
      >

      <div class="main-info__up" v-if="isBestseller">Бесцеллер</div>
      <div class="main-info__up main-info__up--red" v-if="promoBadge">{{ promoBadge }}</div>

      <div class="main-info-text">
        <span class="main-info-text__span">{{ category }}</span>
        <p>{{ title }}</p>
        <span class="main-info-text__span">{{ author }}</span>
        <span class="main-info-text__price">{{ formattedPrice }} ₽</span>

        <div class="main-info-text__rating" v-if="rating || recommendation">
          <div class="main-info-text__yellow" v-if="rating">
            <img :src="getImageUrl('img/Star.svg')" alt="Рейтинг" class="main-info-text__img">
            {{ rating }}
          </div>
          <div class="main-info-text__like" v-if="recommendation">
            <img :src="getImageUrl('img/like.svg')" alt="Рекомендации" class="main-info-text__img">
            {{ recommendation }}% рекомендуют
          </div>
        </div>

        <div class="hero-section__product-card__buttons">
          <button class="hero-section__product-card__button">
            Корзина <img loading="lazy" :src="getImageUrl('img/basket.svg')" alt="Корзина">
          </button>
          <button class="hero-section__product-card__button hero-section__product-card__button--">
            <img loading="lazy" :src="getImageUrl('img/favorite.svg')" alt="Избранное">
          </button>
        </div>
      </div>
    </article>
  </template>

  <script setup>
  import { computed } from 'vue';

  const props = defineProps({
    title: {
      type: String,
      required: true,
      default: "Инвестирование: способы, риски, субъекты : монография"
    },
    author: {
      type: String,
      default: "Майфат А.В."
    },
    category: {
      type: String,
      default: "Корпоративное право"
    },
    price: {
      type: [Number, String],
      default: 4450
    },
    isBestseller: {
      type: Boolean,
      default: true
    },
    promoBadge: {
      type: String,
      default: "1+1=3"
    },
    rating: {
      type: [Number, String],
      default: 4.9
    },
    recommendation: {
      type: [Number, String],
      default: 89
    }
  });

  // Форматирование цены с пробелом
  const formattedPrice = computed(() => {
    return typeof props.price === 'number'
      ? props.price.toLocaleString('ru-RU')
      : String(props.price);
  });

  // Корректное получение путей к изображениям
  const getImageUrl = (name) => {
    return new URL(`/public/img/${name}`, import.meta.url).href;
  };
  </script>

  <style lang="css">
   /* Основные стили карточки */
.main-info__card {
    box-sizing: border-box;
    padding: 10px;
    border: 1px solid rgb(240, 233, 233);
    height: 460px;
    display: flex;
    flex-direction: column;
    gap: 15px;
    background-color: white;
    position: relative;
    flex: 0 0 calc(25% - 20px);
    max-width: calc(25% - 20px);
}

.main-info__book {
    width: 100%;
    max-width: 140px;
    height: 200px;
    margin: 0 auto;
    object-fit: contain;
}

/* Бейджи */
.main-info__up {
    border-radius: 5px;
    padding: 5px 10px;
    background-color: #e8ddfd;
    color: #AC8EE3;
    position: absolute;
    top: 10px;
    left: 15px;
    font-size: 12px;
}

.main-info__up--red {
    top: 40px;
    background-color: #f8d4d4;
    color: #FF4F52;
}

/* Текстовая информация */
.main-info-text {
    display: flex;
    flex-direction: column;
    gap: 10px;
    font-size: 14px;
}

.main-info-text__span {
    font-size: 12px;
    opacity: 0.4;
}

.main-info-text__price {
    font-size: 18px;
    font-weight: bold;
}

/* Рейтинг */
.main-info-text__rating {
    display: flex;
    gap: 10px;
}

.main-info-text__yellow {
    display: flex;
    align-items: center;
    gap: 5px;
    border-radius: 5px;
    background-color: #fff0cb;
    color: #FBC02D;
    padding: 5px 10px;
}

.main-info-text__like {
    display: flex;
    align-items: center;
    gap: 5px;
    border-radius: 5px;
    color: #7986CB;
    background-color: #c7cff7;
    padding: 5px 10px;
}

/* Кнопки */
.hero-section__product-card__buttons {
    display: flex;
    gap: 10px;
    margin-top: auto;
}

.hero-section__product-card__button {
    border-radius: 10px;
    box-shadow: 5px 5px 10px rgba(0, 0, 0, 0.15);
    padding: 10px;
    display: flex;
    align-items: center;
    gap: 5px;
    transition: all 0.3s ease;
    cursor: pointer;
}

.hero-section__product-card__button:hover {
    box-shadow: 5px 5px 10px rgba(248, 112, 0, 0.9);
    transform: scale(1.05);
}

/* Адаптивность */
@media (max-width: 1200px) {
    .main-info__card {
        flex: 0 0 calc(33.333% - 20px);
        max-width: calc(33.333% - 20px);
    }
}

@media (max-width: 900px) {
    .main-info__card {
        flex: 0 0 calc(50% - 20px);
        max-width: calc(50% - 20px);
    }
}

@media (max-width: 600px) {
    .main-info__card {
        flex: 0 0 100%;
        max-width: 100%;
    }
}

@media (max-width: 375px) {
    .main-info
    {
        flex-wrap: wrap;
        padding: 10px;
    }
    .main-info__card {
        height: auto;
        min-height: 430px;
        width: 180px;
    }

    .main-info-text__rating {
        flex-direction: column;
    }
}
  </style>