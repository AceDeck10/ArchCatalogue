<script lang="ts">
  import { Router, Route } from 'svelte-routing';
  import Home from './Home.svelte';
  import Portfolio from './Portfolio.svelte';
  import Footer from './Footer.svelte';


</script>


<Router>
  <Route path="/" component={Home} />
  <Route path="/portfolio" component={Portfolio} />
</Router>

<div>
  <Footer />
</div>