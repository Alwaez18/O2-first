<template>
                        <article class="main-kritery__block">
                        <div class="main-kritery__left">
                            <img loading="lazy"
                            :src="image"
                            alt=""
                            class="main-kritery__img">
                        </div>
                        <div class="main-kritery__right">
                            <h4 class="main-kritery__title">{{TitleText}}</h4>
                            <p class="main-kritery__text">{{ Text }}</p>
                        </div>
                    </article>
</template>
<script setup>
import { computed } from 'vue';
const props= defineProps({
    image: { // Добавлено новое свойство
    type: String,
    default: "/img/oklock.png"
  },
    TitleText:String,
    Text:String,
})
</script>
