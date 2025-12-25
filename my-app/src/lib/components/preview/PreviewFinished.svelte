<script lang="ts">
    export let href: string;
    export let title: string;
    export let context: string;
    export let year: string | number;

    export let mediaType: "image" | "video" = "image";
    export let mediaSrc: string = ""; // image for image-only previews

    export let videoSrcWebm: string = "";
    export let posterSrc: string = "";

    let hover = false;
    let isMobilePlayback = false;

    function updatePlaybackMode() {
        // If device doesn't support hover (typical for touch), treat as mobile playback
        isMobilePlayback = window.matchMedia("(hover: none)").matches;
    }

    // run on mount + on resize/orientation changes
    import { onMount } from "svelte";
    onMount(() => {
        updatePlaybackMode();
        window.addEventListener("resize", updatePlaybackMode);
        return () => window.removeEventListener("resize", updatePlaybackMode);
    });
</script>

<a
    class="preview"
    {href}
    on:mouseenter={() => (hover = true)}
    on:mouseleave={() => (hover = false)}
>
    <div class="image-wrap">
        {#if mediaType === "image"}
            <img class="image" src={mediaSrc} loading="lazy" />
        {:else if isMobilePlayback}
            <!-- Always play on mobile/touch -->
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
            <!-- Hover to play on desktop -->
            {#if hover}
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
                <img class="image" src={posterSrc} loading="lazy" />
            {/if}
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
        <div class="row">
            <div class="table-label">year</div>
            <div class="table-value">{year}</div>
        </div>
    </div>
    <div class="divider"></div>
</a>

<style>
    .preview {
        display: inline-flex;
        flex-direction: column;
        gap: 8px;
        text-decoration: none;
        color: inherit;
    }

    .image-wrap {
        width: 100%;
        aspect-ratio: 1 / 1;
        overflow: hidden;
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
        row-gap: 0px;
    }
    .divider {
        height: 1px;
        background: var(--color-primary);
    }
</style>
