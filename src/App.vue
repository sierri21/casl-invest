<template>
  <div class="main-wrapper">
    <div
      v-if="preload"
      class="preload"
    >
      <video
        src="/video/preloader.mp4"
        autoplay
        muted
        :controls="false"
        @ended="videoHandler"
      />
    </div>

    <index-page v-else />
  </div>
</template>

<script setup>
import IndexPage from '~/pages/index-page.vue'
import { ref } from 'vue'
const preload = ref(false)

// const scale = window.innerWidth / 1440

const videoHandler = () => {
	preload.value = false
}
</script>

<style scoped lang="scss">
.main-wrapper {
  max-width: 100vw;
  width: 100%;
  background: url('/images/background.svg') center 0 / 100vw no-repeat;
  //transform-origin: inherit;
}
.preload {
  height: 100vh;
  width: 100vw;
  display: flex;
  justify-content: center;
  align-items: center;
  background: black;
  video {
    width: 800px;
  }
}
</style>
