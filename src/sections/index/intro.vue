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
  height: initial;
  background: url('/images/background.svg') center / contain no-repeat;
  h1 {
    text-align: center;

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
  // попробовать сделать через fixed
  min-height: 1000px;
  max-width: 100vw;
  padding-top: 340px;
  //overflow-x: hidden;
  //background: gray;
  position: relative;
  width: 100%;
  //z-index: -1;
  //background: red;
  --spacing: 20px;
  .images {
    //max-width: 100vw;
    //background: red;
    //position: absolute;
    //height: 1000px;
    //width: 100%;
  }
  img {
    z-index: 10;
    object-fit: contain;
    &:nth-child(1) {
      position: absolute;
      left: 50%;
      width: 546px;
      transform: translateX(-546px) translateX(-5px) translateY(-150px);
    }
    &:nth-child(2) {
      position: absolute;
      left: 50%;
      //width: 150px;
      object-fit: contain;
      //background: red;
      transform: translateX(calc(-546px - 25px - 100%)) translateY(-50%) translateY(-150px);
      //display: none;
      //width: 12px;

    }
    &:nth-child(3) {
      position: absolute;
      left: 50%;
      width: 546px;
      transform: translateX(5px) translateY(370px) translateY(-150px);
    }
    &:nth-child(4) {
      position: absolute;
      left: 50%;
      object-fit: contain;
      //display: none;
      //clip-path: polygon(0 0, 100px 0, 100px 100%, 0 100%);
      transform: translateX(calc(25px + 546px) ) translateY(720px) translateY(-150px);
    }

  }

}
.sticky {
  position: sticky;
  height: fit-content;
  margin: 0 auto;
  top: 300px;
  padding-bottom: 150px;
  z-index: 20;
  mix-blend-mode: difference;
  background-blend-mode: difference;
}


</style>
