<script lang="ts">
	import ClickOnceBtn from '$lib/components/clickOnceBtn.svelte';
	import PointerMoveDisplay from '$lib/components/pointerMoveDisplay.svelte';
	import Inner from '$lib/components/inner.svelte';
	import Outer from '$lib/components/outer.svelte';
	import BigRedButton from '$lib/components/bigRedButton.svelte';

	function handleMessage({ detail }: { detail?: { text?: string } }) {
		alert(detail?.text);
	}

	function handleClick() {
		alert('clicked');
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
	<section>
		<h2>Event forwarding</h2>
		<Outer on:message={handleMessage} />
	</section>
	<section>
		<h2>Button event forwarding</h2>
		<BigRedButton on:click={handleClick} />
	</section>
</main>
