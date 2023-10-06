<script>
	const name = 'Ujjawal'
	const company = '<i>uCertify<i>'
	const headingId = 'heading'
	let disabled = true
	let status = 'success'
	let isPromoted = true
	let eligible = true
	let age = 18;
</script>

<main>
	<h2 class={status}>Status</h2>
	<h1>Hi {name}</h1>
	<div>{@html company}</div>
	<h2 id={headingId}>A heading</h2>
	<button {disabled}>Bind</button>
	<h2 class={isPromoted ? 'promoted' : ''}>Movie</h2>
	<h2 class:promoted={isPromoted}>Series</h2>
	<h2 class:eligible>Eligible for Driving: {eligible}</h2>
	<h3>Hi Ujjawal Gupta</h3>
	
	{#if age >= 18}
		<h2>You are eligible for Driving</h2>
	{:else}
		<h2>You have to be 18 years old for driving.</h2>
	{/if}

</main>

<style>
	.success {
		color: green;
	}

	.danger {
		color: red;
	}

	.promoted {
		font-style: italic;
	}

	.eligible {
		color: blue;
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