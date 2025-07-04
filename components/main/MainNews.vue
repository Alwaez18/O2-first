<template>
    <article class="main-news__block">
        <div class="main-news__up">
            <img
                loading="lazy"
                :src="image"
                alt=""
                class="main-news__img"
            >
        </div>
        <div class="main-news__info">
            <span class="main-news__date">{{ Date }}</span>
            <h3 class="main-news__title">{{ TitleText }}</h3>
            <p class="main-news__text">{{ Text }}</p>
            <button class="main-news__button">Читать</button>
        </div>
    </article>
</template>

<script setup>
const props = defineProps({
    image: String,
    Date: String,
    TitleText: String,
    Text: String,
    index: {
        type: Number,
        required: true
    }
});
</script>

<style lang="scss">
@media (max-width: 375px) {
    .main-news__block {padding: 10px;}
    .main-news {
        margin: 0 auto;
        display: flex;
        flex-direction: column;
    }
}
</style>