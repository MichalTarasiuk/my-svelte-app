<script lang="ts">
	function getRandomNumber(min: number, max: number) {
		return new Promise((resolve, reject) => {
			const randomNumber = Math.floor(Math.random() * (max - min + 1) + min);

			if (randomNumber >= min && randomNumber <= max) {
				resolve(randomNumber);
			} else {
				reject(new Error('Generated number is out of range.'));
			}
		});
	}

	const range = {
		min: 0,
		max: 100
	};
	const rangeParams = Object.values(range) as [number, number];

	let promise = getRandomNumber(...rangeParams);

	function handleClick() {
		promise = getRandomNumber(...rangeParams);
	}
</script>

<button on:click={handleClick}>generate random number</button>

{#await promise}
	<p>...waiting</p>
{:then number}
	<p>The number is {number}</p>
{:catch error}
	<p style="color: red">{error.message}</p>
{/await}

<!-- If you know that your promise can't reject, you can omit the catch block. You can also omit the
first block if you don't want to show anything until the promise resolves:
{#await promise then number}
	<p>The number is {number}</p>
{/await} -->
