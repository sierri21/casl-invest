<template>
  <section class="intro">
    <div class="intro-background">
      <img
        src="/left.svg"
        alt=""
      >
      <img
        src="/left.svg"
        alt=""
      >
      <img
        src="/right.svg"
        alt=""
      >
      <img
        src="/left.svg"
        alt=""
      >
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
        <span class="yellow-text">blockchain projects</span>, and<br>
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
  min-height: 100vh;
  position: relative;
  h1 {
    text-align: center;
    position: absolute;
    top: 50%;
    left: 50%;
    transform: translateX(-50%);
    width: 1000px;
  }
  &__text {
    p {
      margin-bottom: 50px;
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
  min-height: 1000px;
  max-width: 100vw;
  padding-top: 340px;
  //overflow-x: hidden;
  //background: gray;
  position: relative;
  width: 100%;
  //background: red;
  --spacing: 20px;
  img {
    &:nth-child(1) {
      position: absolute;
      left: 50%;
      transform: translateX(-100%) translateX(-5px) translateY(-150px);
    }
    &:nth-child(2) {
      position: absolute;
      left: 50%;
      transform: translateX(calc(-200% - 25px)) translateY(-50%) translateY(-150px);
    }
    &:nth-child(3) {
      position: absolute;
      left: 50%;
      transform: translateX(5px) translateY(370px) translateY(-150px);
    }
    &:nth-child(4) {
      position: absolute;
      left: 50%;
      transform: translateX(calc(25px + 100%) ) translateY(720px) translateY(-150px);
    }

  }
  //div {
  //  background: red;
  //  margin-top: auto;
  //  margin-bottom: 0;
  //  height: 2px;
  //}

}
.sticky {
  //position: sticky;
  //bottom: 30px;
  //background: red;
  //left: 50%;
}
</style>