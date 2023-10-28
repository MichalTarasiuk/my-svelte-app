<script lang="ts">
	import ClickOnceBtn from '$lib/components/clickOnceBtn.svelte';
	import PointerMoveDisplay from '$lib/components/pointerMoveDisplay.svelte';
	import Inner from '$lib/components/inner.svelte';

	function handleMessage({ detail }: { detail?: { text?: string } }) {
		alert(detail?.text);
	}
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
	<section>
		<h2>Component events</h2>
		<Inner on:message={handleMessage} />
	</section>
</main>
