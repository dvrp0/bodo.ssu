<script lang="ts">
    import "../app.css";
    let { children } = $props();
</script>

<main class="flex p-4 items-center justify-center w-full h-full">
    {@render children()}
</main>