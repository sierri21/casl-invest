<template>
  <section class="contact">
    <button>
      Contact us
    </button>
    <h2>
      Find out which investment product is best for you
    </h2>
  </section>
</template>

<script setup>
</script>

<style scoped lang="scss">
.contact {
  display: flex;
  flex-direction: column;
  align-items: center;

  grid-gap: 40px;
  padding-top: 335px;
  //padding-bottom: 0px;

  text-align: center;

  button {
    font-weight: 300;
    font-size: 100px;
    line-height: 130%;

    color: $Dark-0;
    background: transparent;
    outline: none;
    border: none;

    padding: 27px 100px;
    border-radius: 500px;

    cursor: pointer;

    transition: all .3s ease;

    &:hover {
      background: $Dark-0;
      color: $Dark-100;
    }

    &:active {
      background: #D3D3D3;
    }
  }

  h2 {
    max-width: 1280px;

    color: $Dark-80;
  }
}
</style>