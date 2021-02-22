<script>
    export let id;
    let cols = 2;
</script>

<div class="mt-6 text-xl">Welcome, {id}</div>
<div id="seats" style="--num-columns: {cols}" class="grid grid-flow-row gap-4">
    {#each [...Array(33).keys()].map(i => i += 1) as test}
        <button class="seat">SEAT #{test}</button>
    {/each}
</div>


<style type="text/postcss">
    #seats {
        grid-template-columns: repeat(var(--num-columns), minmax(0, 1fr));
        @apply my-6 w-auto;
    }

    .seat {
        @apply rounded bg-gray-600 px-6 py-3;
    }
</style>

