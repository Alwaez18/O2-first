<!-- components/Footer/FooterBottom.vue -->
<template>
    <div class="footer__bottom">
        <div class="footer__copyright">{{ copyright }}</div>
            <div class="footer__address">{{ address }}</div>
                <div class="footer__legal">
                    <a
                        v-for="(link, index) in legalLinks"
                        :key="index"
                        :href="link.url"
                        class="footer__legal-link"
                    >
                        {{ link.text }}
                    </a>
                </div>
    </div>
  </template>

  <script setup>
  defineProps({
    copyright: {
      type: String,
      default: '© 2020 Издательство «Статут»'
    },
    address: {
      type: String,
      default: 'ул. Лобачевского, 92, корп. 2 119454, г. Москва'
    },
    legalLinks: {
      type: Array,
      default: () => [
        { text: 'Политика конфиденциальности', url: '#' },
        { text: 'Договор оферты', url: '#' }
      ]
    }
  })
  </script>

