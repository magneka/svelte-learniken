<script> 
    import {navn, adresse} from "../../stores/person.js";	
    import FormInput from "./FormInput.svelte";

    let _navn
    navn.subscribe(value => _navn = value) 
    let _adresse
    adresse.subscribe(value => _adresse = value)

    function lagre() {
        console.log("Lagrer form i global state")
        navn.update((n) => _navn)     
        adresse.update((n) => _adresse)        
    }
    //$: nameUpper = navn.toUpperCase()
</script>

<FormInput 
    overskrift="Oppgi navn."
    bind:value={_navn}
    onChange={lagre}
    subcaption="oppgi navn på formen Etternavn, Fornavn"
    size=80
/>
<FormInput 
    overskrift="Oppgi adresse"
    bind:value={_adresse}
    onChange={lagre}
    subcaption="oppgi gatenavn og evt gatenummer"
    size=80
/>

<p>
Du har tastet inn {_navn},  {_adresse}
<button on:click={lagre}>Lagre</button>
</p>

