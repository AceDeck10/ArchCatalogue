<script lang="ts">
  import { Router, Route } from 'svelte-routing';
  import Home from './Home.svelte';
  import Portfolio from './Portfolio.svelte';


</script>


<Router>
  <Route path="/" component={Home} />
  <Route path="/portforlio" component={Portfolio} />
</Router>