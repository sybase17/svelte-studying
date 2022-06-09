<script>
	import Router from "svelte-spa-router";
	import Home from './pages/home/Home.svelte';
	import Temp from './pages/temp/Temp.svelte';


	const routes = {
		'/': Home,
		'/add':Temp
	}

</script>

<header>
	<Router routes={routes}></Router>
</header>

<style>

</style>
	<!-- main  {
		
		text-align: center;
		margin-left:200px;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style> -->