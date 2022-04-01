<script>
import FixedLogo from "$lib/atoms/FixedLogo.svelte";
import NextArrow from "$lib/atoms/NextArrow.svelte";
import Title from "$lib/atoms/Title.svelte";
</script>

<div class="root">
  <div class="circle"></div>
  <section class="logo">
    <FixedLogo />
  </section>
  <section class="botright">
    <Title>Intro to Svelte(Kit)</Title>
  </section>

  <NextArrow slot="next" next="2" />
</div>


<style>
.root {
  background-color: var(--abl-blue);
}

.botright {
  position: fixed;
  color: var(--abl-white);
  bottom: 5rem;
  right: 5rem;
}

.circle {
  display: flex;
  width: 80rem;
  height: 80rem;
  background-color: var(--abl-white);
  border-radius: 50%;
  transform: translate(-30%, -50%);
  overflow: hidden;
  align-items:center;
  justify-items: center;
}
</style>
