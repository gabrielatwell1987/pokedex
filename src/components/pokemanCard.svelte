<script>
    export let pokeman;
</script>

<div class="p-6 bg-gray-100 text-gray-800 text-center rounded-md shadow-sm hover:shadow-md flex flex-col items-center border-2">
    <img src={pokeman.image} alt={pokeman.name} class="h-40 w-40">
    <h2 class="uppercase text-2xl">{pokeman.id}. {pokeman.name}</h2>
</div>