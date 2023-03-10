<script>
  import Report from "$lib/report.svelte";
  import Home from "$lib/home.svelte";
  import { Turnstile } from "svelte-turnstile";
</script>

<div class="hide">
  <Turnstile siteKey="0x4AAAAAAABzM8RBMKZycgnJ" retry="auto" />
</div>
<div class="container">
  <Home />
  <Report />
</div>

<svg id="filters">
  <defs>
    <filter id="threshold">
      <feColorMatrix
        in="SourceGraphic"
        type="matrix"
        values="1 0 0 0 0 0 1 0 0 0 0 0 1 0 0 0 0 0 255 -140"
      />
    </filter>
  </defs>
</svg>


<style>
  .hide {
    display: none;
  }
</style>
