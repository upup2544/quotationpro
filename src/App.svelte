<script>
	import { Router, Route } from "svelte-routing";
	import Home from "./pages/Home.svelte";
	import SideNav from "./layouts/SideNav.svelte";
	import Quotation from "./pages/Quotation.svelte";
	import Customers from "./pages/Customers.svelte";
	import WebSettings from "./pages/WebSettings.svelte";
	import ArchiveBox from "./pages/ArchiveBox.svelte";
	import Global from "./styles/Global.svelte";

	export let url = "";
</script>

<Router url="{url}">
	<main>
		<div class="lhs">
			<SideNav />
		</div>
		<div class="rhs">
			<Route path="/" component="{Home}" />
			<Route path="/home" component="{Home}" />
			<Route path="/quotation" component="{Quotation}" />
			<Route path="/customers" component="{Customers}" />
			<Route path="/web-settings" component="{WebSettings}" />
			<Route path="/archive-box" component="{ArchiveBox}" />
		</div>
	</main>
</Router>

<style>
	main {
		flex-grow: 1;
		display: grid;
		grid-template-columns: 240px 1fr;
		gap: 1em;
		padding: 1em;
	}

	.rhs {
		display: flex;
	}
</style>

<Global />
