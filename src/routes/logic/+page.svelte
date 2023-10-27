<script>
	import ColorPicker from '$lib/components/colorPicker.svelte';
	import Counter from '$lib/components/counter.svelte';
	import RandomNumber from '$lib/components/randomNumber.svelte';
</script>

<main>
	<h1>Logic</h1>
	<section>
		<h2>If blocks, Else blocks and Else-if blocks</h2>
		<Counter />
	</section>
	<section>
		<h2>Each blocks</h2>
		<ColorPicker />
	</section>
	<section>
		<h2>Await blocks</h2>
		<RandomNumber />
	</section>
</main>
