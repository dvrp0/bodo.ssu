<script lang="ts">
    const pages = Object.keys(import.meta.glob("/static/images/pamphlet/*.*", {
        eager: true
    }))
        .map(x => x.replace("/static", ""))
        .sort((a, b) => a.localeCompare(b, undefined, { numeric: true }));
    
</script>

<div class="grid grid-cols-1 mt-4 gap-4">
    {#each pages as src}
        <img {src} loading="lazy" />
    {/each}
</div>