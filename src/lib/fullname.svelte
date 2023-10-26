<script lang="ts">
	import type { ChangeEventHandler } from 'svelte/elements';

	let firstname = '';
	let lastname = '';

	$: fullname = `${firstname} ${lastname}`;

	const handleInputChange: ChangeEventHandler<HTMLInputElement> = ({ target }) => {
		if (!(target instanceof HTMLInputElement)) {
			return;
		}

		if (target.name === 'firstname') {
			firstname = target.value;
		} else if (target.name === 'lastname') {
			lastname = target.value;
		}
	};
</script>

<div>
	<input
		placeholder="Firstname"
		name="firstname"
		bind:value={firstname}
		on:change={handleInputChange}
	/>
	<input
		placeholder="Lastname"
		name="lastname"
		bind:value={lastname}
		on:change={handleInputChange}
	/>

	<p>fullname: {fullname}</p>
</div>
