<template>
  <div class="card">
    <img
      :src="image"
      alt=""
    >
    <h4 v-text="title" />
    <p v-html="text" />
    <div
      class="date"
      v-text="date"
    />
  </div>
</template>

<script setup>
import { defineProps } from 'vue'


defineProps({
	text: {
		type: String,
		default: ''
	},
	title: {
		type: String,
		default: ''
	},
	image: {
		type: String,
		default: ''
	},
	date: {
		type: String,
		default: ''
	}
})
</script>

<style scoped lang="scss">
.card {
  cursor: pointer;
  text-align: start;
  //max-width: 100%;
  overflow: hidden;
  img {
    display: block;
    height: 320px;
    object-fit: cover;
    width: 100%;
    @media screen and (max-width: 1024px) {
      height: auto;
    }
  }
  h4 {
    margin-top: 26px;
    margin-bottom: 8px;
    font-weight: 700;
    font-size: calc(100vw * 26px / (1440px));
    line-height: 130%;
    color: $Dark-10;
    max-width: 388px;
    padding-left: 6px;
  }
  p {
    padding-left: 6px;
    font-weight: 300;
    font-size: calc(100vw * 24px / (1440px));
    line-height: 150%;
    color: $Dark-70;
    max-width: 388px;

    margin-bottom: 12px;
  }
  .date {
    padding-left: 6px;
    font-weight: 300;
    font-size: calc(100vw * 16px / (1440px));
    line-height: 150%;

    color: $Dark-80;
    max-width: 388px;
  }
  &:hover {
    h4 {
      color: #F9A400;;
    }
  }
  &:active h4 {
    color: $Dark-10;
  }

}

</style>
