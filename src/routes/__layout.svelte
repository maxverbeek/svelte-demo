<section>
  <slot></slot>

  {#if $$slots.next}
    <slot name="next"></slot>
  {/if}
</section>

<style>

:global(:root) {
  --abl-blue: #00B1E9;
  --abl-black: #020203;
  --abl-white: #FFFFFF;

  --abl-gray-900: #101010;
  --abl-gray-700: #1b1b1b;
  --abl-gray-400: #717C83;
  --abl-gray-200: #eaeff3;

  font-size: 16px;
}

:global(body) {
  font-family: monospace;
  margin: 0;
}

section {
  overflow: hidden;
  width: 100vw;
  height: 100vh;
}


</style>
