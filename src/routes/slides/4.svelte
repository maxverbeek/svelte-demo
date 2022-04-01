<script>
import FixedLogo from "$lib/atoms/FixedLogo.svelte";
import NextArrow from "$lib/atoms/NextArrow.svelte";

let value = 'nothing yet';
</script>

<FixedLogo />
<section>
  <input bind:value type="text" />

  The value of the box is {value}
</section>

<NextArrow slot="next" next="5" />

<style>
section {
  position: fixed;
  top: 20%;
  right: 20%;
  font-size: 1.5rem;
}
</style>
