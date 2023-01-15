<template>
  <section
    id="services"
    class="key-elements container"
  >
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
        :src="card.img"
        alt=""
      >
      <h3 v-text="card.title" />
      <p v-text="card.text" />
    </div>
  </section>
</template>

<script setup>
const cards = [
	{ img: '/images/key-elems/card1.jpg', title: 'Reliable storage', text: 'Reliable custodial solution allows for more secure storage and access to assets.'},
	{ img: '/images/key-elems/card2.jpg', title: 'Risk hedging', text: 'Crypto derivatives, such as futures and options, are used to minimize volatility risk.'},
	{ img: '/images/key-elems/card3.jpg', title: 'Audited results', text: 'The company\'s financial results from investment activities are auditable and open for review.'}
]
</script>

<style scoped lang="scss">
.key-elements {
  display: grid;
  grid-template-columns: 543px 1fr;
  grid-template-rows: repeat(3, 250px);
  grid-template-areas: 'headline .' 'headline .' 'headline .';
  align-items: center;
  grid-column-gap: 60px;
  padding: 291px 40px 292px;
  @media screen and (max-width: 1439px) {
    grid-template-columns: 470px 1fr;
  }
  @media screen and (max-width: 1240px) {
    grid-template-columns: 400px 1fr;
    grid-template-rows: repeat(3, 170px);
  }
  @media screen and (max-width: 1024px) {
    grid-template-columns: 300px 1fr;
    grid-template-rows: repeat(3, 140px);
  }
  @media screen and (max-width: 768px) {
    grid-template-columns: 150px 1fr;
    grid-column-gap: 20px;
    grid-template-rows: repeat(3, 100px);
    padding-top: 40px;
    padding-bottom: 80px;
  }

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

  @media screen and (max-width: 1240px) {
    grid-template-columns: 200px 1fr;
  }
  @media screen and (max-width: 1024px) {
    grid-template-columns: 150px 1fr;
  }
  @media screen and (max-width: 768px) {
    grid-template-columns: 1fr;
  }

  img {
    grid-area: image;
    display: block;
    //height: 250px;
    width: 100%;
    height: 100%;
    object-fit: cover;
    background: #111111;
  }
  h3 {
    grid-area: title;
    font-style: normal;
    font-weight: 700;
    font-size: min(calc(100vw * 34px / (1440px)), 34px);
    line-height: 130%;
    align-self: end;
  }
  p {
    grid-area: text;
    font-style: normal;
    font-weight: 300;
    font-size: min(calc(100vw * 26px / (1440px)), 26px);
    line-height: 130%;
    color: $Dark-70;
  }
}
</style>
