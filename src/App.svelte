<script>
	import Router from "svelte-spa-router";
	import Home from './pages/home/Home.svelte';
	import Temp from './pages/temp/Temp.svelte';
	import Random from './pages/random/Random.svelte';


	const routes = {
		'/': Home,
		'/add':Temp,
		'/random':Random
	}

</script>

<header>
	<Router routes={routes}></Router>
</header>


<style global lang="postcss">
	@tailwind base;
	@tailwind components;
	@tailwind utilities;
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