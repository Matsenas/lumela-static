<script lang="ts">
    import lumelaLogo from '/lumela.svg'
</script>

<div>
    <img src={lumelaLogo} class="logo" alt="Lumela Logo" />
</div>
<h1 id="title">Lumela</h1>
<h2 id="tagline">
    <p>Experimental design &</p>
    <p>development house</p>
</h2>

<style lang="scss">
    .logo {
      height: 6em;
      padding: 1.5em;
      will-change: filter;
      transition: filter 300ms;
    }
    .logo:hover {
      filter: drop-shadow(0 0 2em #9A9090);
    }

    h2 > p{
        margin: 0;
    }
  
    #title {
      display: none;
    }
</style>