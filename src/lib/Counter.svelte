<script lang="ts">
  let count: number = 0
  const increment = () => {
    count += 1
  }
</script>

<p>You clicked the button {count} times</p>
<button on:click={increment}>
  +1
</button>
