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

<!-- <div class="bg-cover bg-center bg-no-repeat w-full h-[120vh] absolute top-0 z-10 pointer-events-none" style="background-image: url(/images/links/noise.webp);"></div>
<div class="bg-cover bg-center bg-no-repeat w-full h-[120vh] absolute top-0 mix-blend-multiply pointer-events-none" style="background-image: url(/images/links/crumple.webp);"></div>
<div class="bg-cover bg-center bg-no-repeat w-full h-[120vh] absolute top-0 -z-10 pointer-events-none" style="background-image: url(/images/links/paper.webp);"></div> -->
<div class="w-full h-full pt-20 py-10 flex flex-col items-center" style="--height: {screenHeight}px;">
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