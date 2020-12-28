<script>
import { Router, Route } from 'svelte-routing'
import Home from './pages/Home.svelte';
</script>

<Router>
  <Route path="/" component="{Home}" />
</Router>