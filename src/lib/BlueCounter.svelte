<svelte:options customElement="blue-counter" />

<script lang="ts">
  import "./blue.css";

  let count: number = $state(0);
  const increment = () => {
    count += 1;
  };
</script>

<button class="blue" onclick={increment}>
  blue count is {count}
</button>
