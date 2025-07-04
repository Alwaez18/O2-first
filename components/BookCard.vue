<template>
    <article class="main-info__card">
        <img
            loading="lazy"
            :src="imageSrc"
            :alt="title"
            class="main-info__book"
        >
        <div class="main-info__up" v-if="badges.find(b => b.text === 'Бесцеллер')">Бесцеллер</div>
        <div
            class="main-info__up main-info__up--red"
            v-for="badge in badges.filter(b => b.type === 'red')"
            :key="badge.text"
        >
            {{ badge.text }}
        </div>
        <div
            class="main-info__up main-info__up--green"
            v-for="badge in badges.filter(b => b.type === 'green')"
            :key="badge.text"
        >
            {{ badge.text }}
        </div>
        <div class="main-info-text">
            <span class="main-info-text__span">{{ category }}</span>
            <p>{{ title }}</p>
            <span class="main-info-text__span">{{ author }}</span>
            <div v-if="originalPrice" class="price-wrapper">
                <span class="main-info-text__price--old">{{ originalPrice }} ₽</span>
                <span class="main-info-text__price">{{ formattedPrice }} ₽</span>
            </div>
            <span v-else class="main-info-text__price">{{ formattedPrice }} ₽</span>
            <div class="main-info-text__rating" v-if="rating || recommendation">
                <div class="main-info-text__yellow" v-if="rating">
                    <img src="/img/Star.svg" alt="Рейтинг" class="main-info-text__img">
                    {{ rating }}
                </div>
                <div class="main-info-text__like" v-if="recommendation">
                    <img src="/img/like.svg" alt="Рекомендации" class="main-info-text__img">
                    {{ recommendation }}% рекомендуют
                </div>
            </div>
            <div class="hero-section__product-card__buttons">
                <button class="hero-section__product-card__button">
                    Корзина <img loading="lazy" src="/img/basket.svg" alt="Корзина">
                </button>
                <button class="hero-section__product-card__button hero-section__product-card__button--">
                    <img loading="lazy" src="/img/favorite.svg" alt="Избранное">
                </button>
            </div>
        </div>
    </article>
</template>

<script setup>


const props = defineProps({

  imageSrc: {
    type: String,
    default: "/img/book1.png"
  },
  title: {
    type: String,
    required: true
  },
  author: {
    type: String,
    default: ""
  },
  category: {
    type: String,
    default: ""
  },
  formattedPrice: {
    type: [Number, String],
    default: 0
  },
  originalPrice: {
    type: [Number, String],
    default: null
  },
  rating: {
    type: [Number, String],
    default: null
  },
  recommendation: {
    type: [Number, String],
    default: null
  },
  badges: {
    type: Array,
    default: () => []
  },
});

</script>

<style lang="scss">
/* Добавьте этот стиль для старой цены */
.price-wrapper {
  display: flex;
  gap: 10px;
  align-items: center;
}
.main-info-text__price
{
    color:red;
}
.main-info-text__price--old {
  text-decoration: line-through;
  opacity: 0.6;
  font-size: 14px;
}

/* Добавьте стиль для зеленого бейджа */
.main-info__up--green {
  top: 40px;
  background-color: #d4f8e0;
  color: #4CAF50;
}
.main-info
{
    flex-wrap: wrap;
}
</style>