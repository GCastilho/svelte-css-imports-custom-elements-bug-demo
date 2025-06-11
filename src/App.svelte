<script lang="ts">
  import Counter from "./lib/RedCounter.svelte";
  import BlueCounter from "./lib/BlueCounter.svelte";
  import MagentaCounter from "./lib/MagentaCounter.svelte";
  import "./lib/AquaCounter.svelte";
</script>

<main>
  <h1>
    Svelte bug importing foreign CSS into Custom Elements (Web Components)
  </h1>

  <div class="card">
    <section>
      <h3>
        Using <code>import './red.css'</code> and manually inserting a
        CSSStyleSheet on it's shadowRoot using <code>customElement.extend</code>
      </h3>
      <Counter />
      <red-counter></red-counter>
    </section>

    <section>
      <h3>Using <code>import "./blue.css";</code> only</h3>
      <BlueCounter />
      <blue-counter></blue-counter>
    </section>

    <section>
      <h3>Using <code>svelte:head</code> to add stylesheet</h3>
      <MagentaCounter />
      <magenta-counter></magenta-counter>
    </section>

    <section>
      <h3>Manually inserting a link:css to component's shadowRoot</h3>
      <aqua-counter></aqua-counter>
    </section>
  </div>

  <span>See README.md for more details</span>
</main>
