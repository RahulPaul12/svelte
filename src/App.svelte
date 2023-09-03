<script>
	import { Router, Route, Link } from "svelte-routing";
  	import Map from "./pages/Map.svelte";
  	import Layout from "./pages/Layout.svelte";
  	import Chart from "./pages/Chart.svelte";
    export let url = "";
</script>

<main>
	<Router url="{url}">
		<nav>
		   <Link to="/">Layout</Link>
		   <Link to="map">Map</Link>
		   <Link to="chart">Chart</Link>
		 </nav>
		 <div>
		   <Route path="map" component="{Map}" /> 
		   <Route path="/"><Layout/></Route>
		   <Route path="/chart"><Chart/></Route>
		 </div>
	   </Router>
</main>

<style>
	


	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>