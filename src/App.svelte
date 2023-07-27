<script>
	let firstName = 'ikhsan';
	let lastName = 'nur';
	let beltColour = 'black';

	// reactive values
	// start
	$: fullName = `${firstName} ${lastName}`;
	$: {
		console.log(beltColour);
		console.log(fullName);
	}
	// stop

	const handleClick = () => {
		beltColour = 'orange';
	};
	const handleInput = (e) => {
		beltColour = e.target.value;
	};
</script>

<main>
	<!-- <p>{firstName} {lastName} - {beltColour} belt</p> -->

	<p>{fullName} - {beltColour} belt</p>
	<input type="text" bind:value={firstName}>
	<input type="text" bind:value={lastName}>
	<input type="text" bind:value={beltColour}>
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