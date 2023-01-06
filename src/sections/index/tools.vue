<template>
  <section class="tools container">
    <h2 class="tools__headline">
      Balanced investment tools <br>based on your risk appetite
    </h2>
    <div class="tools-card">
      <h3>
        Portfolio management
      </h3>
      <p>
        Discretional long/short strategy<br>
        Yield potential of over 50%<br>
        Denominated in USD or BTC<br>
        Minimum initial investment: USD 50,000<br>
        Minimum investment period 12 months<br>
        Success fee up to 30%
      </p>
    </div>
    <div class="tools-card">
      <h3>
        Index investing
      </h3>
      <p>
        Proprietary CASL INDEX TOP 10<br>
        Only capitalized digital assets<br>
        Monthly rebalancing of the index<br>
        Minimum investment period: 24 months<br>
        Success fee from 0%<br>
        Unlimited asset grow income
      </p>
    </div>
  </section>
</template>

<script setup>
</script>

<style scoped lang="scss">
.tools {
  display: grid;
  grid-template-columns: repeat(2, 1fr);
  grid-template-areas: '. headline' '. headline';
  grid-column-gap: 230px;
  grid-row-gap: 75px;
  align-items: center;
  justify-items: center;
  padding: 120px 0 113px;
  &__headline {
    grid-area: headline;
    max-width: 534px;
  }
}
.tools-card {
  h3 {
    font-style: normal;
    font-weight: 600;
    font-size: 48px;
    line-height: 105%;
    color: #EDEDED;
    margin-bottom: 30px;
    position: relative;
    width: fit-content;
    &:before {
      display: block;
      content: '';
      position: absolute;
      bottom: -4px;
      left: 0;
      width: 100%;
      height: 3px;
      background: linear-gradient(to right, #111111, #F9A400);
      z-index: -1;
    }
  }
   p {
     font-weight: 300;
     font-size: 26px;
     line-height: 31px;
     color: $Dark-70;
     max-width: 482px;
   }
}
</style>