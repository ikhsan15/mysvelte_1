<script>
  let orang = [
    {nama: 'ikhsan', beltColour: 'black', usia: 35, id: 1},
    {nama: 'aida', beltColour: 'brown', usia: 24, id: 2},
    {nama: 'aican', beltColour: 'orange', usia: 40, id: 3}
  ]
</script>

<main>
  <!-- <div>
    <h4>{orang[0].nama}</h4>
    <p>{orang[0].beltColour}</p>
  </div>
  <div>
    <h4>{orang[1].nama}</h4>
    <p>{orang[1].beltColour}</p>
  </div>
  <div>
    <h4>{orang[2].nama}</h4>
    <p>{orang[2].beltColour}</p>
  </div> -->
  
  {#each orang as person (person.id)}
    <div>
      <h4>{person.nama}</h4>
      <p>{person.usia} years old, {person.beltColour} belt.</p>
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