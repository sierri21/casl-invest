<template>
  <section class="intro">
    <h1>
      Today's investments <br>
      affect tomorrow
    </h1>
    <div class="intro__text">
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
      <p>

      </p>
    </div>
  </section>
</template>

<script setup>
</script>

<style scoped lang="scss">
.intro {
  padding-top: 340px;
  min-height: 100vh;
  h1 {
    text-align: center;

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
</style>