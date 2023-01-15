<template>
  <div class="header__wrapper">
    <header class="header ">
      <div class="logo">
        <img
          src="/images/logo.svg"
          alt="logo"
        >
      </div>
      <nav
        v-if="navigation"
        class="navigation"
      >
        <ul class="flex">
          <li
            v-for="link in links"
            :key="link.id"
          >
            <a :href="'#' + link.id">
              {{ link.text }}
            </a>
          </li>
        </ul>
      </nav>
      <a
        href="http://t.me/casl_support"
        target="_blank"
      >
        <button>
          Contact us
        </button>
      </a>
    </header>
  </div>
</template>

<script setup>
import {onMounted, ref} from 'vue'

const navigation = ref(true)

const links = [
	{ text: 'About', id: 'about' },
	{ text: 'Services', id: 'services' },
	{ text: 'Analysis', id: 'analysis' },
]

onMounted(() => {
	window.addEventListener('scroll', () => {
		if (window.scrollY > 50) {
			navigation.value = false
		} else {
			navigation.value = true
		}
	})
})
</script>

<style scoped lang="scss">
.header {
  box-sizing: border-box;

  display: flex;
  justify-content: space-between;
  align-items: center;

  padding: 40px 80px;

  button {
    position: relative;

    font-weight: 500;
    font-size: min(calc(100vw * 16px / (1440px)), 16px);
    line-height: 125%;

    border-radius: 18px;
    border: none;
    outline: none;

    padding: 8px 14px;

    cursor: pointer;

    &:hover {
      background: linear-gradient(45deg, #F9A400 0%, #F9D100 100%);
    }

    &:active {
      background: linear-gradient(45deg, #DA8F00 0%, #DFBB00 100%);
    }

  }
  &__wrapper {
    position: sticky;
    top: 0;

    z-index: 200;

    mix-blend-mode: difference;
  }
}
.navigation {
  margin-left: auto;
  margin-right: 28px;

  ul {
    grid-gap: 32px;
    align-items: center;

    a, button {
      font-style: normal;
      font-weight: 500;
      font-size: min(calc(100vw * 16px / (1440px)), 16px);
      line-height: 125%;
    }
    a {
      color: $Dark-60;
      text-decoration: none;
      display: inline-block;
      padding: 8px 0;
      transition: box-shadow .3s ease;
      &:hover {
        transition: box-shadow .3s ease;
        box-shadow: inset 0px -2px 0px #FFFFFF;
      }
    }

  }
}
.logo {
  height: 40px;
  img {
    mix-blend-mode: difference;
  }

}
</style>
