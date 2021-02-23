<script lang="ts">
  import { Router } from "@roxi/routify";
  import { routes } from "../.routify/routes";
</script>

<Router {routes} />

<style global type="text/postcss">
  @import "../assets/global.css";

  :global(body) {
    @apply font-sans text-white bg-gray-800;
  }

  :global(button) {
    @apply border-none;
  }

  :global(img) {
    @apply border-none;
  }
</style>