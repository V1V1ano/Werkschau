<script lang="ts">
    import Introduction from "../projectElements/Introduction.svelte";
    import ProjectImage from "../projectElements/ProjectImage.svelte";
    import ProjectText from "../projectElements/ProjectText.svelte";

    export let chapter: string;

    // image meta
    export let imageSrc: string;
    export let label: string | null = null;
    export let credit: string | null = null;
    export let caption: string | null = null;

    // text meta
    export let body: string | string[] | null = null;
    export let highlight: string | null = null;
    export let quote: string | null = null;
    export let quoteSource: string | null = null;
    export let linkLabel: string | null = null;
    export let linkHref: string | null = null;
</script>

<div class="image-and-text">
    <ProjectImage src={imageSrc} {label} {credit} {caption} />
    <div class="text-wrap">
        <Introduction {chapter} />
        <div class="inner-text-wrap">
            <ProjectText
                {body}
                {highlight}
                {quote}
                {quoteSource}
                {linkLabel}
                {linkHref}
            />
        </div>
    </div>
</div>

<style>
    .image-and-text {
        display: flex;
        flex-direction: column;
        gap: 18px;
    }

    .text-wrap {
        display: flex;
        flex-direction: column;
        gap: 12px;
    }

    .inner-text-wrap {
        display: flex;
        flex-direction: column;
        gap: 12px;
    }

    @media (min-width: 900px) {
        .image-and-text {
            display: grid;
            grid-template-columns: repeat(2, minmax(0, 1fr));
            align-items: start;
            gap: 118px;
        }

        .inner-text-wrap {
            margin-right: 6rem;
        }
    }
</style>
