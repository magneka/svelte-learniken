<script>
	import {count} from "../../stores/counter.js";	
	import Buttons from "./GlobalCounterButtons.svelte";

	let count_value

	count.subscribe(value => count_value = value)
	
</script>

<h1>Vi har en global teller</h1>

<input type="number" bind:value={count_value} />

<Buttons />

<p>Når vi går til en annen route og tilbake, er verdien uforandret</p>