<script lang="ts">
    export let title: string;
    export let context: string;

    export let mediaType: "image" | "video" = "image";
    export let mediaSrc: string = "";

    export let videoSrcWebm: string = "";
    export let posterSrc: string = "";

    let hover = false;
    let isMobilePlayback = false;

    function updatePlaybackMode() {
        isMobilePlayback = window.matchMedia("(hover: none)").matches;
    }

    import { onMount } from "svelte";
    onMount(() => {
        updatePlaybackMode();
        window.addEventListener("resize", updatePlaybackMode);
        return () => window.removeEventListener("resize", updatePlaybackMode);
    });
</script>

<article
    class="preview"
    on:mouseenter={() => (hover = true)}
    on:mouseleave={() => (hover = false)}
>
    <div class="image-wrap">
        {#if mediaType === "image"}
            <img class="image" src={mediaSrc} loading="lazy" alt="" />
        {:else if isMobilePlayback}
            <video
                class="image"
                muted
                autoplay
                loop
                playsinline
                preload="metadata"
            >
                <source src={videoSrcWebm} type="video/webm" />
            </video>
        {:else if hover}
            <video
                class="image"
                muted
                autoplay
                loop
                playsinline
                preload="metadata"
            >
                <source src={videoSrcWebm} type="video/webm" />
            </video>
        {:else}
            <img class="image" src={posterSrc} loading="lazy" alt="" />
        {/if}
    </div>

    <div class="divider"></div>

    <div class="info-grid">
        <div class="row">
            <div class="table-label">Project</div>
            <div class="table-value">{title}</div>
        </div>
        <div class="row">
            <div class="table-label">Context</div>
            <div class="table-value">{context}</div>
        </div>
    </div>

    <div class="divider"></div>
</article>

<style>
    .preview {
        /* not a link anymore */
        display: flex;
        flex-direction: column;
        gap: 8px;
        color: inherit;
        width: 100%; /* ✅ fill the column */
        max-width: 100%;
    }

    .image-wrap {
        width: 100%;
        height: auto !important; /* ✅ kill inherited heights */
        aspect-ratio: 2 / 1;
        position: relative;
        overflow: hidden; /* ✅ crops correctly */
        display: block; /* ✅ avoid weird inline sizing */
    }

    .image {
        width: 100%;
        height: 100%;
        object-fit: cover;
        display: block;
    }

    .row {
        display: grid;
        grid-template-columns: 140px 1fr;
    }

    .divider {
        height: 1px;
        background: var(--color-primary);
    }

    @media (min-width: 900px) {
        .preview {
            gap: 18px;
        }

        .info-grid {
            display: flex;
            flex-direction: column;
            gap: 4px;
        }
    }
</style>
