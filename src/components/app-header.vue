<template>
  <div class="header__wrapper">
    <header class="header container">
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
            <a href="">
              {{ link.text }}
            </a>
          </li>
        </ul>
      </nav>
      <button>
        Contact us
      </button>
    </header>
  </div>
</template>

<script setup>
import {onMounted, ref} from 'vue'

const navigation = ref(true)

const links = [
	{ text: 'About', id: 'About' },
	{ text: 'Services', id: 'Services' },
	{ text: 'Analysis', id: 'Analysis' },
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
  display: flex;
  box-sizing: border-box;
  justify-content: space-between;
  padding: 40px 40px;
  align-items: center;
  button {
    border-radius: 18px;
    padding: 8px 14px;
    cursor: pointer;
    position: relative;
    border: none;
    font-weight: 500;
    font-size: 16px;
    line-height: 20px;
    outline: none;
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
    mix-blend-mode: difference;
    z-index: 200;
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

  }
}
.logo {
  height: 40px;
  img {
    mix-blend-mode: difference;
  }

}
</style>
