<script>
import NextArrow from "$lib/atoms/NextArrow.svelte";

import { blur } from 'svelte/transition'

let items = [1, 2, 3]

function handleAddItem1() {
  items.push(items.length + 1)
}

function handleAddItem2() {
  items = [ ...items, items.length + 1]
}

</script>

<button on:click={handleAddItem1}>Add more items!</button>
<button on:click={handleAddItem2}>Add more items (for real)!</button>

<ul>
{#each items as item}
<li transition:blur>Item is {item}</li>
{/each}

</ul>

<NextArrow slot="next" next="6" />

<style>
ul {
  font-size: 2rem;
}
</style>
