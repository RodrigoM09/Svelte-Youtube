<script>
	// Binding Text ------------>
	// const name = 'Rodrigo'

	// Binding HTML ------------>
	// const channel = '<b>Svelte Brasil</b>'
	// const hack = `<a href="#" onclick="alert('Te Hackearon!')">Hackeado!</a>`

	// Binding ID ------------>
	// const headingId = 'heading'

	// Binding Attributes ------------>
	// const disabled = true
	// const isPromoted = true
	// const promoted = true

	// Binding Classes ------------>
	// const status = 'danger'

	// Conditional Rendering ------------>
	// const num = 0;

	// List Rendering ------------>
	const names = ['Bruce', 'Clark', 'Diana']
	const fullNames = [
		{ first: 'Bruce', last: 'Wayne' },
		{ first: 'Clark', last: 'Kent' },
		{ first: 'Diana', last: 'Prince' }
	]

</script>

<main>

	<!-- List Rendering -->
		{#each fullNames as name, index}
		<h2>{index + 1} {name.first} {name.last}</h2>
		{/each}
		{#each names as name, index}
		<h1>{index + 1} {name}</h1>
		{/each}

	<!-- Conditional Rendering 
	{#if num === 0 }
	<h2>The number is zero</h2>
	{:else if num < 0}
	<h2>The number is negative</h2>
	{:else if num > 0}
	<h2>The number is </h2>
	{:else}
	<h2>The number is not zero</h2>
	{/if}  -->
	
	<!-- Binding Styles
	<h2 class="underlined">underlined text</h2>
	<h2 class={status}>Status</h2> -->

	<!-- Binding Text
	<h1>Hello {name}</h1> -->

	<!-- Binding Classes
	<h2 class={isPromoted ? 'promoted' : ''}>Movie Title</h2>
	<h2 class:promoted={isPromoted}>Movie Title 2</h2>
	<h2 class:promoted>Movie Title 3</h2> -->

	<!-- Binding HTML
	<p>Welcome to {@html channel}</p>
	<p>{@html hack}</p> -->

	<!-- Binding Properties
	<h1 id={headingId}>Heading</h1> -->

	<!-- Binding Attributes
	<button {disabled}>Bind</button> -->
</main>

<style>
	/* .underlined{
		text-decoration: underline;
	}
	.danger{
		color: red;
	}
	.success{
		color: green;
	}
	.promoted{
		font-style: italic;
	} */
	main {
		text-align: center;
		padding: 1em;
		max-width: 240px;
		margin: 0 auto;
	}

	h1 {
		color: #ff3e00;
		text-transform: uppercase;
		font-size: 4em;
		font-weight: 100;
	}

	@media (min-width: 640px) {
		main {
			max-width: none;
		}
	}
</style>