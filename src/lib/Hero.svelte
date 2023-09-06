<script lang="ts">
    import lumelaLogo from '/lumela.svg'
</script>

<div id="hero-group">
    <div>
        <img src={lumelaLogo} class="logo unselectable" alt="Lumela Logo" />
    </div>
    <h1 id="title">Lumela</h1>
    <h2 id="tagline" class="unselectable">
        <p>Experimental design &</p>
        <p>development house</p>
    </h2>
</div>

<style lang="scss">
    #hero-group {
        display: flex;
        flex-direction: column;
        justify-content: center;
        will-change: transform;
        transition: transform 500ms ease-in-out;
        -webkit-animation: fadein 2s; /* Safari, Chrome and Opera > 12.1 */
        -moz-animation: fadein 2s; /* Firefox < 16 */
        -ms-animation: fadein 2s; /* Internet Explorer */
        -o-animation: fadein 2s; /* Opera < 12.1 */
        animation: fadein 2s;
    }

    #hero-group:hover {
        transform: scale(1.02);
    }
    .logo {
      height: 6em;
      padding: 1.5em;
    }

    h2 {
        margin: 0;
        p{
            margin: 0;
        }
    }
  
    #title {
      display: none;
    }
</style>