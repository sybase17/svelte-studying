<script>
    import { push } from 'svelte-spa-router';
    import Header from "../../components/Header.svelte";
</script>


<Header/>
<main>
    <h1>そのうち</h1>
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