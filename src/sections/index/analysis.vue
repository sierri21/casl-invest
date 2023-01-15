<template>
  <section
    id="analysis"
    class="container analysis"
  >
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

const res = await fetch('https://api.rss2json.com/v1/api.json?rss_url=https://medium.com/feed/@cslinvest2022')
const { items } = await res.json()
// const news = items.slice(0, 3).map(el => {
// 	return {
// 		image: el.thumbnail,
// 		text: el.description && 'Как выцепить нужного человечка? Разбираемся с аналитиками',
// 		title: el.title,
// 		link: el.guid,
// 		date: el.pubDate.split(' ').at(0)
// 	}
// })

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
    color: $Dark-0;
    margin-bottom: 10px;
  }
  p {
    font-weight: 300;
    font-size: min(calc(100vw * 26px / (1440px)), 26px);
    line-height: 130%;
    color: $Dark-80;
  }
}
.news {
  margin-top: 60px;
  display: grid;
  grid-template-columns: repeat(3, 422.65px);
  justify-content: center;
  justify-items: center;
  @media screen and (max-width: 1439px) {
    padding: 0 40px;
    grid-template-columns: repeat(3, 1fr);
  }
  @media screen and (max-width: 768px) {
    padding: 0 40px;
    grid-template-columns: 1fr;
  }

}
</style>
