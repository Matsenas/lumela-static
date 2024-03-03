<script lang="ts">
    import lumelaLogo from '/firn-long.svg'
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
                emojis: ["⚪️"]
            });
        }
  }
</script>

<div id="navbar">
    <!-- svelte-ignore a11y-click-events-have-key-events -->
    <!-- svelte-ignore a11y-no-static-element-interactions -->
    <div id="confetti-button" on:click={startConfetti}>
        <img src={lumelaLogo} class="logo unselectable" alt="Lumela Logo" />
    </div>
</div>

<style lang="scss">
    #confetti-button {
        will-change: transform;
        transition: transform 500ms ease-in-out;
    }

    #confetti-button:hover {
        transform: scale(1.05);
        cursor: pointer;
    }

    #confetti-button:active {
        transform: scale(0.9);
        cursor: pointer;
    }

    #navbar {
        display: flex;
        justify-content: left;
        -webkit-animation: fadein 2s; /* Safari, Chrome and Opera > 12.1 */
        -moz-animation: fadein 2s; /* Firefox < 16 */
        -ms-animation: fadein 2s; /* Internet Explorer */
        -o-animation: fadein 2s; /* Opera < 12.1 */
        animation: fadein 2s;
    }
    .logo {
      height: 3em;
      padding: 1.5em;
    }
</style>