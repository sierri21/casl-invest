<template>
  <section class="key-elements container">
    <h2>
      Key <br>
      elements <br>
      of investing <br>
      with <br>
      Casl Invest
    </h2>
    <div
      v-for="card in cards"
      :key="card.title"
      class="element-card"
    >
      <img
        src=""
        alt=""
      >
      <h3 v-text="card.title" />
      <p v-text="card.text" />
    </div>
  </section>
</template>

<script setup>
const cards = [
	{ img: '', title: 'Reliable storage', text: 'Reliable custodial solution allows for more secure storage and access to assets.'},
	{ img: '', title: 'Risk hedging', text: 'Crypto derivatives, such as futures and options, are used to minimize volatility risk.'},
	{ img: '', title: 'Audited results', text: 'The company\'s financial results from investment activities are auditable and open for review.'}
]
</script>

<style scoped lang="scss">
.key-elements {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-template-rows: repeat(3, 250px);
  grid-template-areas: 'headline .' 'headline .' 'headline .';
  align-items: center;
  grid-column-gap: 60px;
  padding: 100px 0;
  h2 {
    grid-area: headline;
  }
}
.element-card {
  display: grid;
  grid-template-columns: 323px 1fr;
  grid-column-gap: 30px;
  grid-row-gap: 10px;
  height: 250px;
  align-content: center;

  grid-template-areas: 'image title' 'image text';
  img {
    grid-area: image;
    display: block;
    background: red;
    height: 250px;
  }
  h3 {
    grid-area: title;
    font-style: normal;
    font-weight: 700;
    font-size: 34px;
    line-height: 130%;
  }
  p {
    grid-area: text;
    font-style: normal;
    font-weight: 300;
    font-size: 26px;
    line-height: 130%;
    color: $Dark-70;
  }
}
</style>