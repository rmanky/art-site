<script>
    import { metatags } from "@roxi/routify";
    metatags.title = "Seat Select";
    metatags.description = "Description coming soon...";

    let url = "";
</script>

<div class="text-6xl">Seat Select</div>
<div class="flex w-full items-stretch mt-3">
    <input
        bind:value={url}
        type="text"
        placeholder="Enter your ID..."
        class="w-full border-none p-2 bg-gray-600"
    />
    <a href="/seats/{url}" class="rounded bg-green-600 ml-3 py-2 px-6">Go</a>
</div>