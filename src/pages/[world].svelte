<script>
    import { params } from "@roxi/routify";
    import { onMount } from "svelte";
    const world = $params.world;

    let images;

    onMount(async () => {
        let response = await fetch("config.json");
        let data = await response.json();
        images = data[world].images;
        console.log(images);
    });
</script>

<p class="text-4xl mt-3">{world.toUpperCase()}</p>
<a class="text-2xl text-blue-500" href="/">&lt; Back</a>
<div class="masonry lg:mx-24 mx-6 gap-3 mt-3">
    {#if images}
        {#each images as image}
            <img class="item" alt={world} src="/worlds/{world}/{image}" />
        {/each}
    {/if}
    {#if world === "fire"}
        <iframe
            class="item h-100"
            title="360"
            allowfullscreen
            style="border-style:none;"
            src="https://cdn.pannellum.org/2.5/pannellum.htm#panorama=https%3A//i.imgur.com/dsKn9pC.png"
        />
        <iframe
            class="item h-100"
            title="360"
            allowfullscreen
            style="border-style:none;"
            src="https://cdn.pannellum.org/2.5/pannellum.htm#panorama=https%3A//i.imgur.com/TdZYu7h.png"
        />
    {/if}
</div>

<style>
    .masonry {
        /* Masonry container */
        column-count: 1;
    }

    @media (min-width: 768px) {
        .masonry {
            column-count: 2;
        }
    }

    @media (min-width: 1024px) {
        .masonry {
            column-count: 3;
        }
    }

    .item {
        /* Masonry bricks or child elements */
        background-color: #eee;
        display: inline-block;
        margin: 0 0 1em;
        width: 100%;
    }
</style>
