<script>
	import ComponentWithProps from '$lib/components/componentWithProps.svelte';
	import PackageInfo from '$lib/components/packageInfo.svelte';

	const pkg = {
		name: 'svelte',
		speed: 'blazing',
		version: 4,
		website: 'https://svelte.dev'
	};
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
	<section>
		<h2>Spread props</h2>
		<PackageInfo {...pkg} />
	</section>
</main>
