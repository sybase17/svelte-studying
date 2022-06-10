<script>
    import { push } from 'svelte-spa-router';
    import Header from "../../components/Header.svelte";

	let user = {temp: true };

	function toggle() {
		user.temp = !user.temp;
	}

</script>


<Header/>
<span>

</span>
<main>
	{#if user.temp}
		<button on:click={toggle} class="bg-green-600 py-2 px-4 text-white rounded shadow mt-4">ボタン</button>
	{:else}
		<button on:click={toggle} class="bg-green-600 py-2 px-4 text-white rounded shadow mt-4">
			まだ何もありません
		</button>
	{/if}
</main>
  
<style global lang="postcss">
	@tailwind base;
	@tailwind components;
	@tailwind utilities;



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