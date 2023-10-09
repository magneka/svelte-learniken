<script>
    import { onMount } from "svelte";
    import Continent from "./Continent.svelte";
    
    // define the data holding variable
    let continents;

    onMount(async () => {        
        await fetch(`continents.json`)
            .then((r) => r.json())
            .then((data) => {                
                continents = data;
            });
    });
</script>

<main>
    <h1>
        https://blog.logrocket.com/consuming-rest-apis-in-svelte/
    </h1>
    {#if continents}
        {#each continents as continent}
            <ul>
                <li> 
                    <Continent {continent} />                   
                </li>
            </ul>
        {/each}
    {:else}
        <p class="loading">loading...</p>
    {/if}
</main>


