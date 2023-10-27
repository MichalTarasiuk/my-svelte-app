<script>
	let count = 0;

	function increment() {
		count++;
	}

	$: {
		console.log(`The count is ${count}`);
	}
</script>

<button on:click={increment}>
	Clicked {count}
	{count === 1 ? 'time' : 'times'}
</button>

{#if count > 10}
	<p>{count} is greater than 10</p>
{/if}
