<script>
	import { Router, Route } from "svelte-routing";
	import Home from "./pages/Home.svelte";
	import SideNav from "./layouts/SideNav.svelte";

	export let url = "";
</script>

<Router {url}>
	<main>
		<SideNav />
		<div>
			<Route path="/" component={Home} />
		</div>
	</main>
</Router>

<style>
	main {
		display: grid;
		grid-template-columns: 240px 1fr;
		gap: 1em;
	}
</style>
