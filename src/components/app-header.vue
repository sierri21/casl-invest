<template>
<header>
  <nav>
    <ul>
      <li v-for="link in links" :key="link.id">
        {{ link.text }}
      </li>
      <li>
        <button>
          Contact us
        </button>
      </li>
    </ul>
  </nav>
</header>
</template>

<script setup>
const links = [
  {text: 'About', id: 'About'},
  {text: 'Services', id: 'Services'},
  {text: 'Analysis', id: 'Analysis'},
]
</script>

<style scoped>

</style>
