<!-- components/Footer/FooterColumn.vue -->
<template>
  <div class="footer__column">
    <h4 class="footer__column-title">{{ title }}</h4>
    <img
      v-if="showArrow"
      src="/img/strelka.svg"
      alt=""
      class="footer__column-empty"
    >
    <ul class="footer__list">
      <li
        v-for="(item, index) in items"
        :key="index"
        class="footer__item"
      >
        <a
          :href="item.url"
          class="footer__link"
          :class="{
            'footer__link--email': item.type === 'email',
            'footer__link--phone': item.type === 'phone'
          }"
        >
          {{ item.text }}
        </a>
      </li>
    </ul>
  </div>
</template>

<script setup>
defineProps({
  title: {
    type: String,
    required: true
  },
  items: {
    type: Array,
    required: true,
    validator: items => items.every(item =>
      typeof item.text === 'string' &&
      typeof item.url === 'string'
    )
  },
  showArrow: {
    type: Boolean,
    default: true
  }
})
</script>

