<script>
import { fade } from 'svelte/transition'

async function randomPromise() {

  await new Promise(r => setTimeout(r, 2000))

  return 5

}

let promise = randomPromise()

</script>

{#await promise}
  <h2 transition:fade>Waiting for the promise to resolve</h2>
{:then val}
  <h2 transition:fade>The value of the promise is {val}</h2>
{:catch err}
  <h2>Apaprently I cannot write a sleep function</h2>
{/await}

<style>

</style>
