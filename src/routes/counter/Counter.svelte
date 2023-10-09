<script>
    let count = 0
</script>

<h1>Typisk eksempel på teller</h1>

<input type="number" bind:value={count} />

<button on:click={() => (count += 1)}>Øke med 1</button>
<button on:click={() => (count -= 1)}>Redusere med en</button>
