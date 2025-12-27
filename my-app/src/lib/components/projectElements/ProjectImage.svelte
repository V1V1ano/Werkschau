<script lang="ts">
    export let src: string;

    // optional overlays + caption
    export let label: string | null = null; // e.g. "EXPLORATORY VIEW"
    export let credit: string | null = null; // e.g. "@ALEXANDER MOLKENTHIN"
    export let caption: string | null = null;
</script>

<figure class="project-image">
    <div class="media">
        <img class="img" {src} loading="lazy" />

        {#if label}
            <div class="explanatory-tag">{label}</div>
        {/if}

        {#if credit}
            <div class="creator-tag">{credit}</div>
        {/if}
    </div>

    {#if caption}
        <div class="caption-wrapper">
            <div class="caption">{caption}</div>
            <div class="caption arrow">↰</div>
        </div>
    {/if}
</figure>

<style>
    .project-image {
        margin: 0;
        display: flex;
        flex-direction: column;
        gap: 8px;
    }

    .media {
        width: 100%;
        aspect-ratio: 1 / 1; /* ✅ always square */
        position: relative;
        overflow: hidden;
    }

    .img {
        width: 100%;
        height: 100%;
        display: block;
        object-fit: cover;
    }

    /* overlays */
    .explanatory-tag {
        position: absolute;
        top: 12px;
        left: 12px;
        padding: 4px 10px;
        background-color: rgba(255, 255, 255, 0.6);
        border: 1px solid var(--color-primary);
    }

    .creator-tag {
        position: absolute;
        right: 12px;
        bottom: 12px;
        padding: 0px 6px;
        background-color: rgba(255, 255, 255, 0.6);
    }

    .caption-wrapper {
        display: grid;
        grid-template-columns: 1fr auto; /* text | arrow */
        gap: 8px;
        align-items: start;
        padding-right: 2px;
    }

    .arrow {
        display: inline-block; /* important for transform */
        transform: rotate(90deg);
    }
</style>
