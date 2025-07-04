<script setup>
import { ref } from 'vue';
import HeaderBottom from '../components/header/header-bottom.vue';
import HeaderMain from '../components/header/header-main.vue';
import HeaderTop from '../components/header/header-top.vue';
import HeroSectionAction from '../components/hero-section/hero-section-action.vue';
import HeroSectionBlocks from '../components/hero-section/hero-section-blocks.vue';
import HeroSectionCard from '../components/hero-section/hero-section-card.vue';
import MainHeader from '../components/main/main-header.vue';
import MainSearch from '../components/main/main-search.vue';
import MainNew from '../components/main/MainNews.vue';
import FooterTop from '../components/footer/footerTop.vue';
import FooterBotomn from '../components/footer/footerBotomn.vue';
import NewsSlider from '/components/main/NewsSlider.vue';

const MainKriterys = ref([
	{
		image:"/img/oklock.png",
		titleText:"Быстрая доставка",
		Text:"Доставим бесплатно от 2000 ₽ по всей России"
	},
	{
		image:"/img/oklock.png",
		titleText:"Быстрая доставка",
		Text:"Доставим бесплатно от 2000 ₽ по всей России"
	},
	{
		image:"/img/oklock.png",
		titleText:"Быстрая доставка",
		Text:"Доставим бесплатно от 2000 ₽ по всей России"
	},
	{
		image:"/img/oklock.png",
		titleText:"Быстрая доставка",
		Text:"Доставим бесплатно от 2000 ₽ по всей России"
	},
	{
		image:"/img/oklock.png",
		titleText:"Быстрая доставка",
		Text:"Доставим бесплатно от 2000 ₽ по всей России"
	},
]);



const mainNew = ref([
  {
    image: "/img/news.png",
    TitleText: "Заголовок 1",
    Date: "16 июня 2020",
    Text: "Текст 1...",
  },
  {
    image: "/img/news.png",
    TitleText: "Заголовок 2",
    Date: "16 июня 2020",
    Text: "Текст 2...",
  },
  {
    image: "/img/news.png",
    TitleText: "Заголовок 3",
    Date: "16 июня 2020",
    Text: "Текст 3...",
  }
]);
</script>





<template>
	<header class="header">
		<div><HeaderTop/></div>
		<div><HeaderMain/></div>
		<div><HeaderBottom/></div>
	</header>

	<main class="main">
		<section class="hero-section">
			<div class="container">
				<div class="hero-section__grid">
					<HeroSectionAction />
						<HeroSectionBlocks />
						<HeroSectionCard
							title="Акция дня"
							image="/img/book day.png"
							bookTitle="Другая книга"
							author="Иванов И.И."
							price="3200"
						/>
				</div>
			</div>
		</section>
		<div class="container"><MainHeader titleText="Новые Поступления"/></div>
		<section class="main">
			<div class="container">
				<div class="main-info">
					<BookCard
						title="Инвестирование: способы, риски, субъекты : монография"
						imageSrc="/img/book.png"
						author="Майфат А.В."
						category="Корпоративное право"
						:formattedPrice="4450"
						:rating="4.9"
						:recommendation="89"
						:badges="[
						{ text: 'Бесцеллер', type: 'default' },
						{ text: '1+1=3', type: 'red' }
						]"
					/>
					<BookCard
						title="Инвестирование: способы, риски, субъекты : монография"
						imageSrc="/img/book1.png"
						author="Майфат А.В."
						category="Корпоративное право"
						:formatedprice="4450"
						:rating="4.9"
						:recommendation="89"
						:badges="[
						{ text: 'Новинка', type: 'green' }
						]"
					/>
					<BookCard
						imageSrc="/img/book2.png"
						title="Инвестирование: способы, риски, субъекты : монография"
						author="Майфат А.В."
						category="Корпоративное право"
						:formattedPrice="984"
						:originalPrice="1284"
						:rating="4.9"
						:recommendation="89"
						:badges="[
							{ text: 'Бесцеллер', type: 'default' },
							{ text: '1+1=3', type: 'red' }
						]"
					/>
					<BookCard
						imageSrc="/img/book2.png"
						title="Инвестирование: способы, риски, субъекты : монография"
						author="Майфат А.В."
						category="Корпоративное право"
						:formattedPrice="984"
						:originalPrice="1284"
						:rating="4.9"
						:recommendation="89"
						:badges="[
							{ text: 'Бесцеллер', type: 'default' },
							{ text: '1+1=3', type: 'red' }
						]"
					/>
				</div>
				<div><MainSearch /></div>
			</div>
		</section>
			<div class="container"><MainHeader titleText="Готовяться к выходу" /></div>
		<section class="main">
			<div class="container">
				<div class="main-info">
					<BookCard
						title="Инвестирование: способы, риски, субъекты : монография"
						imageSrc="/img/book.png"
						author="Майфат А.В."
						category="Корпоративное право"
						:formattedPrice="4450"
						:rating="4.9"
						:recommendation="89"
						:badges="[
						{ text: 'Бесцеллер', type: 'default' },
						{ text: '1+1=3', type: 'red' }
						]"
					/>
					<BookCard
						title="Инвестирование: способы, риски, субъекты : монография"
						imageSrc="/img/book1.png"
						author="Майфат А.В."
						category="Корпоративное право"
						:formatedprice="4450"
						:rating="4.9"
						:recommendation="89"
						:badges="[
						{ text: 'Новинка', type: 'green' }
						]"
					/>
					<BookCard
						imageSrc="/img/book2.png"
						title="Инвестирование: способы, риски, субъекты : монография"
						author="Майфат А.В."
						category="Корпоративное право"
						:formattedPrice="984"
						:originalPrice="1284"
						:rating="4.9"
						:recommendation="89"
						:badges="[
							{ text: 'Бесцеллер', type: 'default' },
							{ text: '1+1=3', type: 'red' }
						]"
					/>
					<BookCard
						imageSrc="/img/book2.png"
						title="Инвестирование: способы, риски, субъекты : монография"
						author="Майфат А.В."
						category="Корпоративное право"
						:formattedPrice="984"
						:originalPrice="1284"
						:rating="4.9"
						:recommendation="89"
						:badges="[
							{ text: 'Бесцеллер', type: 'default' },
							{ text: '1+1=3', type: 'red' }
						]"
					/>
				</div>
				<div class="main-info__all-books">
					<a href="" class="main-info__link">Показать все книги раздела</a>
				</div>
				<div class="main-kritery">
					<MainKritery
					v-for="(item, index) in MainKriterys"
					:key="index"
					:image="item.image.default"
					:titleText="item.titleText"
					:Text="item.Text"
					/>
				</div>
					<MainHeader titleText="Новости" />
				<div class="main-news">
					<NewsSlider :news-list="mainNew" />

				</div>
			</div>
		</section>
	</main>
	<FooterTop/>

	<footer class="footer">
		<div class="container">
			<div><Footer /></div>
			<div><FooterBotomn /></div>
		</div>
	</footer>
</template>
