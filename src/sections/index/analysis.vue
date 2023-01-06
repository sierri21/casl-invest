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
        :title="card.title"
        :text="card.text"
      />
    </div>
  </section>
</template>

<script setup>
import AppNewsCard from '~/components/app-news-card.vue'

const news = [
	{img: '', text: '1', title: '1', date: '22'}
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
}
</style>