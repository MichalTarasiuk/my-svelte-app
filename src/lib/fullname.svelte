<script lang="ts">
	import type { ChangeEventHandler } from 'svelte/elements';

	let firstname = '';
	let lastname = '';

	$: fullname = firstname + ' ' + lastname;

	const firstnameChangeEventHandler: ChangeEventHandler<HTMLInputElement> = ({ target }) => {
		if (target instanceof HTMLInputElement) {
			firstname = target.value;
		}
	};

	const lastnameChangeEventHandler: ChangeEventHandler<HTMLInputElement> = ({ target }) => {
		if (target instanceof HTMLInputElement) {
			firstname = target.value;
		}
	};
</script>

<div>
	<input placeholder="Firstname" bind:value={firstname} on:change={firstnameChangeEventHandler} />
	<input placeholder="Lastname" bind:value={lastname} on:change={lastnameChangeEventHandler} />

	<p>fullname: {fullname}</p>
</div>
