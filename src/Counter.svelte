<script>
  import Button from './Button.svelte'
  export let count = 0;

  $: content = count > 5 ? 'Lookin good...' : `The count's kinda low. Ain't it?`
  $: color = count > 5 ? 'limegreen' : 'red'
</script>

<div>
  <h2 style="color: {color}"  >{content}</h2>
  <div>
    <Button on:click="{() => count -= 1}">-</Button>
    <h2 style="color: {color}">{count}</h2>
    <button on:click="{() => count += 1}">+</button>
  </div>
</div>

<style>
	div div {
		display: flex;
    justify-content: center;
	}

	button {
		margin: 1rem;
	}
</style>