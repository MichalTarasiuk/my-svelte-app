<script lang="ts">
	// import type { MouseEventHandler } from 'svelte/elements';

	let m = { x: 0, y: 0 };

	// const handleMove: MouseEventHandler<HTMLDivElement> = (event) => {
	// 	m.x = event.clientX;
	// 	m.y = event.clientY;
	// };
</script>

<p>The pointer is at {m.x} x {m.y}</p>

<div
	on:pointermove={(e) => {
		m = { x: e.clientX, y: e.clientY };
	}}
	role="presentation"
/>

<style>
	div {
		max-width: 400px;
		height: 100px;
		background-color: red;
	}
</style>
