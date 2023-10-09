<script>
  // create a prop continent
  export let continent
</script>

<h1>{continent.name}</h1>
<small>
    Population: <b>{continent.population}</b>
</small><br />
<small>
    Antall land: <b>{continent.no_of_countries}</b>
</small><br />
<small>
    Areal: <b>{continent.area}</b>
</small><br />

<style>
  h1 {
    font-size: 1.4em;
    margin: 0;
    display: block;
  }
</style>
