<template>
        <section class="main-header">
                <div class="main-content">
                    <div class="main-content__header">
                        <h5 class="main-content__title">{{ titleText }}</h5>
                        <nav class="main-content-nav">
                            <button class="main-content-nav__button">> </button>
                            <button class="main-content-nav__button main-content-nav__button--rotate">></button>
                        </nav>
                    </div>
                </div>
        </section>
</template>
<script setup>
defineProps({
  titleText: String // Текст для h5
})
</script>
<style>
    .main-content__title{ font-size: 36px; }
    @media(max-width:375px){
        .main-header
        {
            padding: 0;
        }
    }
</style>