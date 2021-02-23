<script>
    import { metatags } from "@roxi/routify";
    metatags.title = "Hostile Environments";
    metatags.description = "An online art gallery...";

    let url = "";

    let list = [
        {
            "title": "COVID-19",
            "folder": "covid",
            "hero": "1.png"
        },
        {
            "title": "D-DAY",
            "folder": "dday",
            "hero": "1.png"
        },
    ]
</script>

<div class="my-3 text-4xl">Hostile Environments</div>
<div class="flex flex-wrap justify-center gap-6 mx-6">
    {#each list as world}
        <div class="w-full md:w-1/3 lg:w-1/4">
            <a href="/{world.folder}">
                <img
                    class="rounded-t-lg w-full"
                    alt="covid"
                    src="worlds/{world.folder}/{world.hero}"
                />
                <div class="bg-gray-600 rounded-b-lg  p-3">
                    <header class="flex items-center justify-between">
                        <p class="text-xl">{world.title}</p>
                        <p class="text-md">02/22/2021</p>
                    </header>
                </div>
            </a>
        </div>
    {/each}
</div>
