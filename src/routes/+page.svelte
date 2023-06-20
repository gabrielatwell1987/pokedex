<script>
    import {pokemon} from '../stores/pokestore';
    import PokemanCard from '../components/pokemanCard.svelte';

    let searchTerm = '';
    let filteredPokemon = [];

    $: {
        if (searchTerm) {
            filteredPokemon = $pokemon.filter(pokeman => pokeman.name.toLowerCase().includes(searchTerm.toLowerCase()));
        } else {
            filteredPokemon = [...$pokemon];
        }
    }
</script>

<svelte:head>
    <title>POKEDEX</title>
</svelte:head>

<h1 class="text-5xl font-extrabold text-center my-8 uppercase">pokedex</h1>
<br>
<input type="text" placeholder="Search Pokemon" class="w-full rounded-md text-lg p-4 border-2 border-gray-700" bind:value={searchTerm}>
<br><br>
<div class="grid gap-4 md:grid-cols-2 grid-cols-1 py-4">
    {#each filteredPokemon as pokeman}
        <PokemanCard {pokeman} />
    {/each}
</div>