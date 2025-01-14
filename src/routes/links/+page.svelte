<script lang="ts">
    import {
        PUBLIC_BODO_INSTAGRAM,
        PUBLIC_BODO_PAMPHLET,
        PUBLIC_PLAY_INSTAGRAM,
        PUBLIC_PLAY_YOUTUBE
    } from "$env/static/public";

    let screenHeight = $state(0);
    $effect(() => {
        screenHeight = window.innerHeight;
        console.log(screenHeight);
    });
</script>

<div class="background z-10" style="background-image: url(/images/links/noise.webp);"></div>
<div class="background mix-blend-multiply" style="background-image: url(/images/links/crumple.webp);"></div>
<div class="background -z-10" style="background-image: url(/images/links/paper.webp);"></div>
<div class="w-full sm:max-w-[25rem] max-h-full flex flex-col justify-center items-center" style="--height: {screenHeight}px;">
    <img class="py-10" src="/images/links/logo.webp" />
    <div class="flex flex-col justify-center items-center pt-10 gap-4">
        <a href={PUBLIC_BODO_INSTAGRAM} target="_blank">
            <img src="/images/links/bodo-insta.webp" />
        </a>
        <a href={PUBLIC_BODO_PAMPHLET} target="_blank">
            <img src="/images/links/bodo-pam.webp" />
        </a>
        <a href={PUBLIC_PLAY_INSTAGRAM} target="_blank">
            <img src="/images/links/play-insta.webp" />
        </a>
        <a href={PUBLIC_PLAY_YOUTUBE} target="_blank">
            <img src="/images/links/play-youtube.webp" />
        </a>
    </div>
</div>

<style>
    .background {
        @apply bg-cover bg-center bg-no-repeat w-full h-[120vh] fixed top-0 pointer-events-none
    }
</style>