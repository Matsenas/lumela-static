<script lang="ts">
    import lumelaLogo from '/lumela.svg'
    import JSConfetti from 'js-confetti'

    const searchParams = new URLSearchParams(window.location.search);



    let jsConfetti = new JSConfetti()

    function startConfetti() {
        if (searchParams.get('ri') == "ho") {
            jsConfetti.addConfetti({
                emojis: ["R", "I", "H", "O"]
            });
        } else {
            jsConfetti.addConfetti({
                emojis: ["🐈"]
            });
        }
  }
</script>

<div id="hero-group">
    <!-- svelte-ignore a11y-click-events-have-key-events -->
    <!-- svelte-ignore a11y-no-static-element-interactions -->
    <div id="confetti-button" on:click={startConfetti}>
        <img src={lumelaLogo} class="logo unselectable" alt="Lumela Logo" />
    </div>
    <h1 id="title">Lumela</h1>
    <h2 id="tagline" class="unselectable">
        <p>Experimental design &</p>
        <p>development house</p>
    </h2>
</div>

<style lang="scss">
    #confetti-button {
        will-change: transform;
        transition: transform 300ms ease-in-out;
    }

    #confetti-button:hover {
        transform: scale(1.1);
        cursor: pointer;
    }

    #confetti-button:active {
        transform: scale(0.9);
        cursor: pointer;
    }

    #hero-group {
        display: flex;
        flex-direction: column;
        justify-content: center;
        -webkit-animation: fadein 2s; /* Safari, Chrome and Opera > 12.1 */
        -moz-animation: fadein 2s; /* Firefox < 16 */
        -ms-animation: fadein 2s; /* Internet Explorer */
        -o-animation: fadein 2s; /* Opera < 12.1 */
        animation: fadein 2s;
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