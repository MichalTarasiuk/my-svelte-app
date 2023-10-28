<script>
	import NumericInput from '$lib/components/numericInput.svelte';
	import TextInput from '$lib/components/textInput.svelte';
	import CheckboxInput from '$lib/components/checkboxInput.svelte';
	import QuestionForm from '$lib/components/questionForm.svelte';
</script>

<main>
	<h1>Bindings</h1>
	<section>
		<h2>Text inputs</h2>
		<TextInput />
	</section>
	<section>
		<h2>Numeric inputs</h2>
		<NumericInput />
	</section>
	<section>
		<h2>Checkbox inputs</h2>
		<CheckboxInput />
	</section>
	<section>
		<h2>Select bindings</h2>
		<QuestionForm />
	</section>
</main>
