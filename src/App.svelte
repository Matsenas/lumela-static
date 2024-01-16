<script lang="ts">
  import Navbar from './lib/Navbar.svelte'
  import Hero from './lib/Hero.svelte'
  import Footer from './lib/Footer.svelte'
</script>

<main>
  <Navbar/>
  <Hero/>
  <!-- <Footer/> -->
</main>

<style lang="scss">
  main {
    height: 100%;
    display: flex;
    flex-direction: column;
  }
</style>
