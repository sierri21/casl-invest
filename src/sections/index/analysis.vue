<template>
  <section class="container analysis">
    <h2>
      Analysis
    </h2>
    <p>
      Monthly market reviews and results evaluation
    </p>
    <div class="news">
      <app-news-card
        v-for="card in news"
        :key="card.title"
        v-bind="card"
      />
    </div>
  </section>
</template>

<script setup>
import AppNewsCard from '~/components/app-news-card.vue'

const news = [
	{image: '/images/lorem/new1.jpg', text: 'Как выцепить нужного человечка? Разбираемся с аналитиками', title: 'Когда абонент не абонент', date: 'Today'},
	{image: '/images/lorem/new2.jpg', text: 'Прямо вот с соседнего стола доносится, свежачок', title: 'Платеж увидел, запустил в работу', date: 'Nov 27, 2022'},
	{image: '/images/lorem/new3.jpg', text: 'Учимся избегать залетов', title: 'Капуста на дороге не валяется, пару месяцев придется за спасибо', date: 'Nov 26, 2022'},
]
</script>

<style scoped lang="scss">
.analysis {
  text-align: center;
  h2 {
    font-weight: 300;
    font-size: 100px;
    line-height: 130%;
    color: $Dark-0;
    margin-bottom: 10px;
  }
  p {
    font-weight: 300;
    font-size: 26px;
    line-height: 130%;
    color: $Dark-80;
  }
}
.news {
  margin-top: 60px;
  display: grid;
  grid-template-columns: repeat(3, 422.65px);
  justify-content: center;
}
</style>
