<script>
	let age = 18;
	const names = ['ujjawal', 'naman', 'nayan']
	const fullNames = [
		{firstName: 'Ujjawal', lastName: 'Gupta'},
		{firstName: 'Rishabh', lastName: 'Sehgal'},
		{firstName: 'Yojan', lastName: 'Saini'}
	]

	const foodItems = ['Burger', 'Pizza', 'Pasta', 'Ravioli']
</script>

<main>
	{#if age >= 18}
		<h2>You are an adult now!!</h2>
	{:else if age <= 0}
		<h2>Enter a valid age</h2>
	{:else}
		<h2>You're still a child</h2>
	{/if}

	<!-- for each loop in array -->
	{#each names as name, index}
		<h2>{index+1}. Hi, {name}</h2>
	{/each}
	
	<!-- for each loop in object -->
	{#each fullNames as name, index}
		<h2>{index+1} {name.firstName} {name.lastName}</h2>
	{/each}

	{#each foodItems as item, index (index)}
		<h2>{index} {item}</h2>
	{/each}

</main>

<style>
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