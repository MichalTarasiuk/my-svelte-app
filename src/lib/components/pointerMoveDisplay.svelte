<script lang="ts">
	import type { MouseEventHandler } from 'svelte/elements';

	let m = { x: 0, y: 0 };

	const handleMove: MouseEventHandler<HTMLDivElement> = (event) => {
		m.x = event.clientX;
		m.y = event.clientY;
	};
</script>

<p>The pointer is at {m.x} x {m.y}</p>

<div on:mousemove={handleMove} role="presentation" />

<style>
	div {
		position: absolute;
		inset: 0;
	}
</style>
