<!-- components/Footer.vue -->
<template>
  <footer class="footer">
    <div class="container">
      <div class="footer__main">
        <FooterColumn
          title="Покупателям"
          :items="[
          { text: 'Наша почта', url: '#' },
          { text: 'Оплата и доставка', url: '#' },
          { text: 'Вопросы и ответы', url: '#' },
          { text: 'Контакты', url: '#' }
          ]"
        />

        <FooterColumn
          title="Издательство"
          :items="[
          { text: 'О компании', url: '#' },
          { text: 'Авторам', url: '#' },
          { text: 'Вакансии', url: '#' }
          ]"
        />

        <FooterColumn
          title="Книги"
          :items="[
          { text: 'Все категории', url: '#' },
          { text: 'Бестселлеры', url: '#' },
          { text: 'Новинки', url: '#' },
          { text: 'Скидки и акции', url: '#' }
          ]"
        />

        <FooterColumn
          title="Прайс-лист"
          :items="[
          { text: 'Скачать прайс-лист', url: '#' },
          { text: 'PDF, 12 Мb', url: '#' }
          ]"
        />

        <FooterColumn
          title="Телефон и Email"
          :items="[
          { text: 'market@estatut.ru', url: 'mailto:market@estatut.ru', type: 'email' },
          { text: '8 (968) 660-65-50', url: 'tel:89686606550', type: 'phone' }
          ]"
        />
      </div>

      <FooterBottom />
    </div>
  </footer>
</template>

<script setup>

</script>
