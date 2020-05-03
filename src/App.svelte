<script>
	import Counter from './Counter.svelte';
	import List from './NumbersList.svelte';
	let numbers = [0,1,2,3,4,5]
</script>

<main>
	<Counter count={12} />
	<List numbers={numbers} />
</main>

<style>
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>