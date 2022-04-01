<script>
import FixedLogo from "$lib/atoms/FixedLogo.svelte";
import NextArrow from "$lib/atoms/NextArrow.svelte";

let count = 0;

$: derived = count * 2;

function handleClick() {
  count += 1
}

</script>

<FixedLogo />
<NextArrow slot="next" next="4" />

<section>
  <button on:click={handleClick}>Increment a count</button>
  {derived}
</section>

<style>
section {
  font-size: 3rem;
  inset: 50%;
  position: fixed;
  bottom: 10%;
}
</style>
