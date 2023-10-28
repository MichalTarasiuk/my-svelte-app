<script>
	import ClickOnceBtn from '$lib/components/clickOnceBtn.svelte';
	import PointerMoveDisplay from '$lib/components/pointerMoveDisplay.svelte';
</script>

<main>
	<h1>Events</h1>
	<section>
		<h2>DOM Events</h2>
		<PointerMoveDisplay />
	</section>
	<section>
		<h2>Event modifiers</h2>
		<ClickOnceBtn />
	</section>
</main>
