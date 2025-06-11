<svelte:options customElement="magenta-counter" />

<script lang="ts">
  let count: number = $state(0);
  const increment = () => {
    count += 1;
  };
</script>

<button class="magenta" onclick={increment}>
  magenta count is {count}
</button>

<svelte:head>
  <link rel="stylesheet" href="/magenta.css" />
</svelte:head>
