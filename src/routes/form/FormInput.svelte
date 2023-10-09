<script> 
    export let overskrift;
    export let value;
    export let subcaption;
    export let size
    export let onChange;
</script>

<p class="caption">{overskrift}:</p>
<input 
    class="inp" type="text" 
    bind:value={value} 
    on:change={onChange}
    size={size} />
<p class="subcaption">{subcaption}</p>

<style>
    .caption {
        font-size: 34px;        
        margin-bottom: 4px;
    }
    .inp {             
        margin-bottom: 4px;
    }
    .subcaption {
        font-size: 12px;        
        margin-top: 0px;
        padding-top: 0px;
    }
</style>


