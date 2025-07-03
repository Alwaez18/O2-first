<template>
     <section class="header-main">  <!-- Блок -->
            <div class="container">
              <div class="header-main__content">  <!-- Элемент -->
                <div class="header-main__search">  <!-- Элемент -->
                    <img src="/img/katalog.svg" alt="" class="header-main__mobile">
                  <img src="/img/logo (2).svg" alt="Логотип" class="header-main__logo">
                  <div class="header-main__search-wrapper">
                    <input type="search" class="header-main__search-input" placeholder="Что будем искать?" src="../img/search.svg">
                    <button class="header-main__search-button">
                      <img src="/img/search.svg" alt="Поиск" class="header-main__search-icon">
                      <span class="header-main__search-text">Искать</span>
                    </button>
                    <img src="/img/korzina.svg" alt="" class="header-main__mobile">
                  </div>
                </div>

                <nav class="header-main__nav">  <!-- Элемент -->
                  <div class="header-main__nav-item">  <!-- Элемент -->
                    <img src="/img/otlozheno.svg" alt="Отложено" class="header-main__nav-icon">
                    <a href="#" class="header-main__nav-link">Отложено</a>
                  </div>
                  <div class="header-main__nav-item">
                    <img src="/img/login.svg" alt="Войти" class="header-main__nav-icon">
                    <a href="#" class="header-main__nav-link">Войти</a>
                  </div>
                  <div class="header-main__nav-item">
                    <img src="/img/korzina.svg" alt="Корзина" class="header-main__nav-icon">
                    <a href="#" class="header-main__nav-link">Корзина</a>
                     <!-- Элемент -->
                  </div>
                </nav>
              </div>
            </div>
          </section>
</template>