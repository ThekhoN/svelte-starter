<script>
  export let count = 0;
</script>

<div>
  <button on:click="{() => count -= 1}">-</button>
  <h2>{count}</h2>
  <button on:click="{() => count += 1}">+</button>
</div>

<style>
	div {
		display: flex;
	}

	button {
		margin: 1rem;
	}
</style>