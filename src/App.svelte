<script>
	const name = 'Rodrigo'
	const channel = '<b>Svelte Brasil</b>'
	const hack = `<a href="#" onclick="alert('Te Hackearon!')">Hackeado!</a>`
	const headingId = 'heading'
	const disabled = true
	const status = 'danger'
	const isPromoted = true
	const promoted = true

</script>

<main>
	<h2 class="underlined">underlined text</h2>
	<h2 class={status}>Status</h2>
	<h1>Hello {name}</h1>
	<h2 class={isPromoted ? 'promoted' : ''}>Movie Title</h2>
	<h2 class:promoted={isPromoted}>Movie Title 2</h2>
	<h2 class:promoted>Movie Title 3</h2>
	<p>Welcome to {@html channel}</p>
	<p>{@html hack}</p>
	<h1 id={headingId}>Heading</h1>
	<button {disabled}>Bind</button>
</main>

<style>
	.underlined{
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
	}
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