<template>
  <main>
    <div>
      <app-header />
      <intro />
      <tools />
      <key-elements />
      <analysis />
    </div>
      
    <contact />
    <app-footer />
  </main>
</template>

<script setup>
import AppHeader from '~/components/app-header.vue'

import Intro from '~/sections/index/intro.vue'
import Tools from '~/sections/index/tools.vue'
import KeyElements from '~/sections/index/key-elements.vue'
import Analysis from '~/sections/index/analysis.vue'
import Contact from '~/sections/index/contact.vue'
import AppFooter from '~/components/app-footer.vue'
</script>

<style scoped>

</style>