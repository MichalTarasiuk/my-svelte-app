<script>
	import Description from '$lib/ui/description.svelte';

	let name = 'Svelte';

	let src = '/svelte.png';
	let alt = 'svelte';
</script>

<main>
	<h1>Hello {name.toUpperCase()}</h1>
	<img {src} alt="{alt} logo" />
	<Description />
</main>

<style>
	main {
		display: flex;
		flex-direction: column;
		align-items: center;
		gap: 0.5rem;
		padding-inline: 20rem;
	}

	img {
		width: 100px;
	}

	/* Stles don't leak in
	p {
		color: red;
	} */
</style>
