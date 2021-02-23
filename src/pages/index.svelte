<script>
    import { onMount } from "svelte";
    import { metatags } from "@roxi/routify";
    metatags.title = "Hostile Environments";
    metatags.description = "An online art gallery...";

    let list;

    onMount(async () => {
        let response = await fetch("config.json");
        let data = await response.json();
        list = data;
    });
</script>

<div class="my-3 text-4xl">Hostile<br>Environments</div>
<div class="flex flex-wrap justify-center gap-6 mx-6">
    {#if list}
        {#each Object.entries(list) as [world, data]}
            <div class="w-full md:w-1/3 lg:w-1/4">
                <a href="/{world}">
                    <img
                        class="rounded-t-lg w-full"
                        alt="covid"
                        src="worlds/{world}/{data.images[0]}"
                    />
                    <div class="bg-gray-600 rounded-b-lg  p-3">
                        <header class="flex items-center justify-between">
                            <p class="text-xl">{data.name}</p>
                            <p class="text-md">{data.date}</p>
                        </header>
                    </div>
                </a>
            </div>
        {/each}
    {/if}
</div>
