<script lang="ts">
    import Introduction from "../projectElements/Introduction.svelte";

    import ProjectImage from "../projectElements/ProjectImage.svelte";

    export let imageSrc: string;
    export let chapter: string;
    export let text: string = "";

    export let label: string | null = null;
    export let credit: string | null = null;
    export let caption: string | null = null;
</script>

<div class="image-and-text">
    <ProjectImage src={imageSrc} {label} {credit} {caption} />
    <div class="text-wrap">
        <Introduction {chapter} />
        <div class="body">{text}</div>
    </div>
</div>

<style>
    .image-and-text {
        display: flex;
        flex-direction: column;
        gap: 18px;
    }

    .image-wrap {
        width: 100%;
        aspect-ratio: 1 / 1; /* ✅ square */
        overflow: hidden;
    }

    .image {
        width: 100%;
        height: 100%; /* ✅ fill the square */
        display: block;
        object-fit: cover;
    }

    .text-wrap {
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
    }
</style>
