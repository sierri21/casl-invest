<template>
  <div class="card">
    <img
      src=""
      alt=""
    >
    <h4>
      {{ title }}
    </h4>
    <p>
      {{ text }}
    </p>
    <div class="date" />
  </div>
</template>

<script setup>
// eslint-disable-next-line no-undef
defineProps({
	text: String,
	title: String
})
</script>

<style scoped>

</style>