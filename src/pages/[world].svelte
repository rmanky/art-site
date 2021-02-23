<script>
    import { params } from "@roxi/routify";
    const world = $params.world;

    let images = {
        covid: [
            "1.png",
            "2.gif",
            "3.png",
            "4.gif",
            "5.png",
            "6.png",
            "7.png",
            "8.png",
            "9.png",
            "10.png",
            "11.png",
        ],
        dday: [
            "1.png",
            "2.gif",
            "3.png",
            "4.png",
            "5.png",
            "6.png",
            "7.png",
            "8.png",
            "9.png",
            "10.png",
            "11.png",
            "12.png",
            "13.png",
            "14.png",
            "15.png",
            "16.png",
            "17.png",
            "18.png",
            "19.png",
        ],
    };
</script>

<p class="text-4xl my-3">{world.toUpperCase()}</p>
<div class="masonry lg:mx-36 mx-6 gap-3">
    {#each images[world] as image}
        <img class="item" alt={world} src="/worlds/{world}/{image}" />
    {/each}
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
