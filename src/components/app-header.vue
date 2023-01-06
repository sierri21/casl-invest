<template>
<header class="header container">
  <div class="logo">
    <img src="" alt="logo">
  </div>
  <nav class="navigation">
    <ul class="flex">
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
  { text: 'About', id: 'About' },
  { text: 'Services', id: 'Services' },
  { text: 'Analysis', id: 'Analysis' },
]
</script>

<style scoped lang="scss">
.header {
  display: flex;
  justify-content: space-between;
  margin-top: 40px;
}
.navigation {
  ul {
    grid-gap: 32px;
  }
}

</style>
