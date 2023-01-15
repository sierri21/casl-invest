<template>
  <section class="intro">
    <div class="intro-background">
      <h1 class="sticky">
        Today's investments <br>
        affect tomorrow
      </h1>
    </div>

    <div class="intro__text container">
      <p>
        Casl Invest is a financial<br>
        company that focuses<br>
        on finding and selecting<br>
        the most promising<br>
        alternative investment<br>
        instruments, which<br>
        include
        <span class="yellow-text">digital assets</span>,<br>
        <span class="yellow-text">blockchain projects</span> and<br>
        <span class="yellow-text">decentralized finance</span>.
      </p>
      <p>
        We successfully apply the experience of classical<br>
        investment to the market of virtual assets and <span class="yellow-text">steadily <br>outperform</span>
        the standard financial products, whether<br>
        ETF or investments in commodities.<br>
      </p>
      <p />
    </div>
  </section>
</template>

<script setup>
</script>

<style scoped lang="scss">
.intro {
  padding-top: 0;

  max-width: 100vw;
  height: initial;

  position: relative;

  h1 {
    text-align: center;
    max-width: 1000px;
  }

  &__text {
    position: absolute;
    bottom: 82px;
    left: 50%;
    max-width: 1440px;
    padding: 0 80px;
    transform: translateX(-50%);
    box-sizing: border-box;
    @media screen and (max-width: 1024px) {
      bottom: 50px;
      left: 0;
      max-width: 100vw;
      transform: none;
      padding-left: 40px;
    }
    @media screen and (max-width: 500px) {
      bottom: 0px;
      left: 0;
      max-width: 100vw;
      transform: none;
      padding-left: 40px;
    }

    p {
      margin-bottom: 50px;
      @media screen and (max-width: 768px) {
        margin-bottom: 20px;
      }

      &:first-child {
        max-width: 480px;
      }

      &:last-child {
        max-width: 1080px;
      }
    }
  }
}

.intro-background {

  height: calc((2009px * 100vw) / (1440px));
  max-width: 100vw;
  width: 100%;
  position: relative;
}

.sticky {
  position: sticky;
  height: fit-content;
  margin: 0 auto;
  top: 339px;

  padding-bottom: 973px;
  z-index: 20;
  mix-blend-mode: difference;
  background-blend-mode: difference;
  @media screen and (max-width: 1024px){
    padding-bottom: 550px;
    top: 200px;
  }
  @media screen and (max-width: 500px){
    padding-bottom: 300px;
    top: 100px;
  }
}


</style>
