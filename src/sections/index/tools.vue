<template>
  <section
    id="about"
    ref="tools"
    class="tools container"
  >
    <h2 class="tools__headline">
      Balanced investment tools <br>based on your risk appetite
    </h2>
    <div class="tools-card">
      <h3 :style="{'--visible': isElementVisible ? '100%' : '0%'}">
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
      <h3 :style="{'--visible': isElementVisible ? '100%' : '0%'}">
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

import {ref} from 'vue'
import { useIntersectionObserver } from '@vueuse/core'

const tools = ref(null)
const isElementVisible = ref(false)

// eslint-disable-next-line no-unused-vars
const { stop } = useIntersectionObserver(
	tools,
	([{ isIntersecting }]) => {
		isElementVisible.value = isIntersecting
	},
)
</script>

<style scoped lang="scss">
.tools {
  display: grid;
  grid-template-columns: 516px 534px;
  grid-template-areas: '. headline' '. headline';
  grid-column-gap: 230px;
  grid-row-gap: 28px;
  align-items: center;
  justify-items: center;
  padding: 148px 40px 113px;
  &__headline {
    grid-area: headline;
    max-width: 534px;
    //display: none;
  }
}
.tools-card {
  justify-self: start;
  padding-top: 40px;
  h3 {
    font-style: normal;
    font-weight: 600;
    font-size: calc(100vw * 48px / (1440px));
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
      width: var(--visible);
      height: 3px;
      background: linear-gradient(to right, #111111, #F9A400);
      transition: width 2s .3s ease ;
      //transform: translateX(var(--visible));
    }
  }
   p {
     font-weight: 300;
     font-size: calc(100vw * 26px / (1440px));
     line-height: 170%;
     color: $Dark-70;
     max-width: 482px;
   }
}
</style>
