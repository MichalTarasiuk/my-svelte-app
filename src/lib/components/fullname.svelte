<script lang="ts">
	let firstname = '';
	let lastname = '';

	$: fullname = `${firstname} ${lastname}`;
</script>

<div>
	<input placeholder="Firstname" name="firstname" bind:value={firstname} />
	<input placeholder="Lastname" name="lastname" bind:value={lastname} />

	<p>fullname: {fullname}</p>
</div>
