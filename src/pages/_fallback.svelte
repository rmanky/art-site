<script>
  import { url } from "@roxi/routify";
</script>

<div class="text-10xl">404</div>
<div class="text-2xl">
  Page not found.
  <!-- link to the parent folder of _fallback.svelte -->
  <a class="text-blue-500 underline" href={$url("../")}>Go back</a>
</div>
