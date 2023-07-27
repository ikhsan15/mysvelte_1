<script>
  let orang = [
    {nama: 'ikhsan', beltColour: 'black', usia: 35, id: 1},
    {nama: 'aida', beltColour: 'brown', usia: 24, id: 2},
    {nama: 'aican', beltColour: 'orange', usia: 40, id: 3}
  ];

  const handleClick = (id) => {
    // delete the person from orang
    orang = orang.filter((person) => person.id != id)
  }
</script>

<main>  
  {#each orang as person (person.id)}
    <div>
      <h4>{person.nama}</h4>
      <p>{person.usia} years old, {person.beltColour} belt.</p>
      <!-- <button on:click={() => {console.log('click me'); }}>delete</button> -->
      <button on:click={() => {handleClick(person.id)}}>delete</button>      
    </div>
    {:else}
      <p>There are no peaplo to show ...</p>
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