<script>
	let name = 'Svelte';

	let src = '/svelte.png';
	let alt = 'svelte';
</script>

<main>
	<h1>Hello {name.toUpperCase()}</h1>
	<img {src} alt="{alt} logo" />
</main>

<style>
	main {
		display: flex;
		flex-direction: column;
		align-items: center;
	}

	img {
		width: 100px;
	}
</style>
