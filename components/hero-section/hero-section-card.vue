<template>
    <article class="hero-section__product-card">
      <!-- Верхняя часть карточки -->
      <div class="hero-section__product-card__up">
        <h3 class="hero-section__product-card__title">{{ title }}</h3>
        <time :datetime="datetime" class="hero-section__product-card__time">{{ timeText }}</time>
      </div>

      <!-- Основное содержимое -->
      <div class="hero-section__product-card__main">
        <img
          loading="lazy"
          :src="image"
          :alt="title"
          class="hero-section__product-card__img"
        >
      </div>

      <!-- Нижняя часть карточки -->
      <div class="hero-section__product-card__low">
        <span class="hero-section__product-card__desription">{{ category }}</span>
        <span class="hero-section__product-card__desription hero-section__product-card__desription--black">{{ bookTitle }}</span>
        <span class="hero-section__product-card__desription">{{ author }}</span>
        <span class="hero-section__product-card__desription hero-section__product-card__desription--sale">
          {{ formattedPrice }} ₽
        </span>
      </div>

      <!-- Кнопки -->
      <div class="hero-section__product-card__buttons">
        <button class="hero-section__product-card__button">
          Корзина <img src="/img/basket.svg" alt="Корзина">
        </button>
        <button class="hero-section__product-card__button hero-section__product-card__button--">
          <img src="/img/favorite.svg" alt="Избранное">
        </button>
      </div>
    </article>
  </template>

  <script setup>
  import { computed } from 'vue';

  const props = defineProps({
    title: {
      type: String,
      default: "Книга дня"
    },
    datetime: {
      type: String,
      default: new Date().toISOString()
    },
    timeText: {
      type: String,
      default: new Date().toLocaleTimeString()
    },
    image: {
      type: String,
      default: "/img/book-day.png"
    },
    category: {
      type: String,
      default: "Корпоративное право"
    },
    bookTitle: {
      type: String,
      default: "Инвестирование: способы, риски, субъекты : монография"
    },
    author: {
      type: String,
      default: "Майфат А.В."
    },
    price: {
      type: [Number, String],
      default: 4450
    }
  });

  const formattedPrice = computed(() => {
    return typeof props.price === 'number'
      ? props.price.toLocaleString('ru-RU')
      : String(props.price);
  });
  </script>
