<script>
	import Counter from '$lib/components/counter.svelte';
	import Fullname from '$lib/components/fullname.svelte';
	import Summary from '$lib/components/summary.svelte';
</script>

<main>
	<h1>Reactivity</h1>
	<section>
		<h2>Assignments</h2>
		<Counter />
	</section>
	<section>
		<h2>Declarations</h2>
		<Fullname />
	</section>
	<section>
		<h2>Updating arrays and objects</h2>
		<Summary />
	</section>
</main>
