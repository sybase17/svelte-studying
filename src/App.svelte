<script>
	import Header from './components/Header.svelte'
</script>

<Header/>

<main>
	<h1>中心確認</h1>
</main>

<style>
	main  {
		
		text-align: center;
		margin-left:200px;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>