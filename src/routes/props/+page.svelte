<script>
	import ComponentWithProps from '$lib/components/componentWithProps.svelte';
</script>

<main>
	<h1>Props</h1>
	<section>
		<h2>Declaring props</h2>
		<ComponentWithProps prop="value" />
	</section>
	<section>
		<h2>Default values</h2>
		<ComponentWithProps />
	</section>
</main>
