<svelte:options
  customElement={{
    tag: "aqua-counter",
    // shadow: "none",
    extend(svelteCustomElementClass) {
      return class extends svelteCustomElementClass {
        constructor() {
          super();
          const link = document.createElement("link");
          link.rel = "stylesheet";
          link.href = "/aqua.css";
          this.shadowRoot?.appendChild(link);
        }
      };
    },
  }}
/>

<script lang="ts">
  let count: number = $state(0);
  const increment = () => {
    count += 1;
  };
</script>

<button class="aqua" onclick={increment}>
  aqua count is {count}
</button>
