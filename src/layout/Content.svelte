<script>
    import { Route, Router, Link } from "svelte-routing";
    import Home from "../routes/home/Home.svelte";
    import Counter from "../routes/counter/Counter.svelte";
    import GlobalCounter from "../routes/globalcounter/GlobalCounter.svelte";
  import Continents from "../routes/continents/Continents.svelte";
  import Form from "../routes/form/Form.svelte";
    let url = "/";
    let path = location.pathname;
</script>

<Router {url}>
    <div>
        <Route path="/counter" component={Counter} />
        <Route path="/counterglobal" component={GlobalCounter} />
        <Route path="/continents" component={Continents} />
        <Route path="/form" component={Form} />
        <Route path="/" component={Home} />
        <Route path="*" component={Home} />
    </div>
</Router>