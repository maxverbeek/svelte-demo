<script>
import FixedLogo from "$lib/atoms/FixedLogo.svelte";
import NextArrow from "$lib/atoms/NextArrow.svelte";

import { blur } from "svelte/transition"
let shown = false

</script>

<FixedLogo />
<NextArrow slot="next" next="3" />

<ul class="righttext" on:click={() => shown = !shown}>
  <li>Written in "normal" HTML, javascript and CSS</li>
  <li>Added sugaring for HTML if-statements, loops, etc</li>
  <li>Nice component structure</li>
  {#if shown}
    <li transition:blur>Animations</li>
  {/if}
</ul>

<style>
.righttext {
  position: fixed;
  right: 15%;
  top: 40%;
  font-size: 2rem;
}
</style>
