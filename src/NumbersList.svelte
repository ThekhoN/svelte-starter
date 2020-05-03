<script>
  export let numbers;
  let color = 'pink'

  const getColorForNumber = number => number % 2 === 0 ? 'pink' : 'grey'
</script>

<div>
  <h3>List</h3>
  <ul>
  {#each numbers as number}  
    {#if number % 2 === 0} 
    <p style="color: {getColorForNumber(number)}">Even: {number}</p> 
    {:else}
    <p style="color: {getColorForNumber(number)}">Odd: {number}</p>
    {/if}
  {/each}
  </ul>
</div>
