<script lang="ts">
  import { Router } from "@roxi/routify";
  import { routes } from "../.routify/routes";
</script>

<Router {routes} />

<style global type="text/postcss">
  :global(body) {
    @apply text-white font-sans bg-gray-800;
  }
  
  :global(button, input) {
      @apply text-lg rounded border-none;
  }
</style>