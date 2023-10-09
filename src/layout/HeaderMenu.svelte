<script>
    import { Router, Link } from "svelte-routing";
</script>

<Router>
    <div class="wrapper">
        <Link to="/">Home</Link>   
        <Link to="/counter">Counter</Link>
        <Link to="/counterglobal">Counter global</Link>
        <Link to="/continents">Continents</Link>   
        <Link to="/form">Form</Link>   
    
    </div>
</Router>

<style>
    
    .wrapper {        
        padding-top: 18px;        
    }

    :global(a) {
        color: white;
        font-size: 25px;
        text-decoration: none;
        padding-right: 6px;
    }

    :global(a:hover) {
        color: white;
        font-size: 25px;
        text-decoration: underline;
    }
    
</style>