<script>
	let num = 0

	function subtract() {
		num -= 1;
	}

	const add = () => {
		num += 1
	}

	function handleEvent(count) {
		num += count
	}
</script>

<main>
	<!-- inline event handler -->
	<button on:click={() => num -= 1}>-</button>
	<!-- <label class="label" for="number">{num}</label> -->
	<input id="number" type="text" value={num}>
	
	<button on:click={add}>+</button>

	<button on:click={() => handleEvent(4)}>+</button>
</main>

<style>
	.label {
		display: inline;
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