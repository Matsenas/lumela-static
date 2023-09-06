<script lang="ts">
  import Hero from './lib/Hero.svelte'
  import Footer from './lib/Footer.svelte'
  import ComingSoon from './lib/ComingSoon.svelte'
</script>

<main>
  <Hero/>
  <Footer/>
  <ComingSoon/>
</main>

<style lang="scss">
  main {
    height: 100%;
    display: flex;
    justify-content: center;
    align-items: center;
  }
</style>
