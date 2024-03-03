<script lang="ts">
  import Navbar from './lib/Navbar.svelte';
  import Hero from './lib/Hero.svelte';
  import Footer from './lib/Footer.svelte';
  import { Router, Route } from 'svelte-routing';
  import Leaderboard from './Leaderboard.svelte'; // Import your Leaderboard component
</script>

<main>
  <Navbar/>
  <Router>
    <Route path="/" component={Hero} />
    <Route path="/leaderboard" component={Leaderboard} />
  </Router>
  <!-- <Footer/> -->
</main>

<style lang="scss">
  main {
    height:  100%;
    display: flex;
    flex-direction: column;
  }
</style>
