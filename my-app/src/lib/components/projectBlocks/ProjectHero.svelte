<script lang="ts">
    import KeyArea from "../KeyArea.svelte";
    type KeyAreaVariant = "ui" | "conceptual" | "narratives" | "speculative";
    import ButtonSmall from "../Buttons/ButtonSmall.svelte";

    export let keyArea: KeyAreaVariant;
    export let title: string;
    export let subtitle: string;
    export let scope: string;
    export let tools: string;
    export let collaborators: string | string[];
    export let context: string | string[];
    export let year: string | number;
    export let linkHref: string = "";
    export let linkLabel: string;

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

<div class="hero">
    <div class="image-wrap">
        {#if mediaType === "image"}
            <img class="image" src={mediaSrc} loading="lazy" />
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
            <img class="image" src={posterSrc} loading="lazy" />
        {/if}
    </div>

    <div class="textual-part">
        <div class="top">
            <div class="project-headline">{title}</div>
            <div class="sub-headline">{subtitle}</div>
        </div>
        <div class="bottom">
            <KeyArea variant={keyArea} />
            <div class="divider"></div>

            <div class="row">
                <div class="table-label">Scope</div>
                <div class="table-value">{scope}</div>
            </div>
            <div class="row">
                <div class="table-label">Tools</div>
                <div class="table-value">{tools}</div>
            </div>

            <div class="divider"></div>

            <div class="row">
                <div class="table-label">Collaborators</div>
                <div class="table-value">
                    {#if Array.isArray(collaborators)}
                        {#each collaborators as person}
                            <div>{person}</div>
                        {/each}
                    {:else}
                        {collaborators}
                    {/if}
                </div>
            </div>
            <div class="row">
                <div class="table-label">Context</div>
                <div class="table-value">{#if Array.isArray(context)}
                        {#each context as setting}
                            <div>{setting}</div>
                        {/each}
                    {:else}
                        {context}
                    {/if}</div>
            </div>
            <div class="row">
                <div class="table-label">year</div>
                <div class="table-value">{year}</div>
            </div>

            <div class="divider"></div>
            <div class="row">
                <div class="table-label">link</div>
                <div class="table-value">
                    <ButtonSmall href={linkHref} type="external"
                        >{linkLabel}</ButtonSmall
                    >
                </div>
            </div>
        </div>
    </div>
</div>

<style>
    .hero {
        display: flex;
        flex-direction: column;
        gap: 18px;
    }

    .image-wrap {
        width: 100%;
        aspect-ratio: 1 / 1;
        overflow: hidden;
        position: relative; /* ✅ needed for overlay */
    }

    .image {
        width: 100%;
        height: 100%;
        object-fit: cover;
        display: block;
    }

    .top {
        display: flex;
        flex-direction: column;
        gap: 18px;
        margin-bottom: 56px;
    }

    .bottom {
        display: flex;
        flex-direction: column;
        gap: 8px;
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

    @media (min-width: 900px) {
        .hero {
            display: grid;
            grid-template-columns: repeat(2, minmax(0, 1fr));
            align-items: start;
            gap: 118px;
        }
    }
</style>
