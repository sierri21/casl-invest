<template>
  <div class="header__wrapper">
    <header class="header container">
      <div class="logo">
        <img
          src="/images/logo.svg"
          alt="logo"
        >
      </div>
      <nav class="navigation">
        <ul class="flex">
          <li
            v-for="link in links"
            :key="link.id"
          >
            <a href="">
              {{ link.text }}
            </a>
          </li>
          <li>
            <button>
              Contact us
            </button>
          </li>
        </ul>
      </nav>
    </header>
  </div>
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
  //padding: 40px 40px 0;
  padding: 40px 0;
  align-items: center;
  &__wrapper {
    position: fixed;
    left: 0;
    right: 0;
    background: #111111;
    z-index: 200;
    box-shadow: 0 10px 20px 10px #111111 ;

  }
}
.navigation {
  ul {
    grid-gap: 32px;
    align-items: center;
    a, button {
      font-style: normal;
      font-weight: 500;
      font-size: 16px;
      line-height: 20px;
    }
    a {
      color: $Dark-60;
      text-decoration: none;
      &:hover {
        text-decoration: underline;
      }
    }
    button {
      border-radius: 18px;
      padding: 8px 14px;
      cursor: pointer;
      position: relative;
      border: none;
      outline: none;
      &:hover {
        background: linear-gradient(45deg, #F9A400 0%, #F9D100 100%);
      }
      &:active {
        background: linear-gradient(45deg, #DA8F00 0%, #DFBB00 100%);
      }

    }
  }
}
.logo {
  height: 40px;
}
</style>
