<script lang="ts">
    import { beforeNavigate, goto } from "$app/navigation";
    import { PUBLIC_BOOK_LINK } from "$env/static/public";
    import { MetaTags } from "svelte-meta-tags";

    const name = "숭실대학교 극예술연구회 제103회 정기공연 「보도지침」";

    beforeNavigate(() => {
        goto(PUBLIC_BOOK_LINK);
    })
</script>

<MetaTags
    title={name}
    openGraph={{
        url: "https://bodo-ssu.pages.dev/book",
        title: name,
        images: [
            {
                url: "https://bodo-ssu.pages.dev/images/links/og-thumbnail.webp",
                width: 1200,
                height: 627,
                alt: name
            }
        ],
        siteName: name
    }}
/>