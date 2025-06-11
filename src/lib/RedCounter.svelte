<svelte:options
  customElement={{
    tag: "red-counter",
    // shadow: "none",
    extend(svelteCustomElementClass) {
      return class extends svelteCustomElementClass {
        constructor() {
          super();
          const sheet = new CSSStyleSheet();
          sheet.replaceSync(redCss);
          this.shadowRoot?.adoptedStyleSheets.push(sheet);
        }
      };
    },
  }}
/>

<script lang="ts">
  import "./red.css";
  import redCss from "./red.css?raw";

  let count: number = $state(0);
  const increment = () => {
    count += 1;
  };
</script>

<button class="red" onclick={increment}>
  red count is {count}
</button>
