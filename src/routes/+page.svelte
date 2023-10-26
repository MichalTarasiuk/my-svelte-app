<script>
	let name = 'Svelte';

	let src = '/svelte.png';
	let alt = 'svelte';
</script>

<main>
	<h1>Hello {name.toUpperCase()}</h1>
	<img {src} alt="{alt} logo" />
</main>
