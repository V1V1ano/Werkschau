<script lang="ts">
  export let href: string;
  export let title: string;
  export let context: string;
  export let year: string | number;

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

<a
  class="preview"
  href={href}
  on:mouseenter={() => (hover = true)}
  on:mouseleave={() => (hover = false)}
>
  <div class="image-wrap">
    {#if mediaType === "image"}
      <img class="image" src={mediaSrc} loading="lazy" />
    {:else if isMobilePlayback}
      <video class="image" muted autoplay loop playsinline preload="metadata">
        <source src={videoSrcWebm} type="video/webm" />
      </video>
    {:else}
      {#if hover}
        <video class="image" muted autoplay loop playsinline preload="metadata">
          <source src={videoSrcWebm} type="video/webm" />
        </video>
      {:else}
        <img class="image" src={posterSrc} loading="lazy" />
      {/if}
    {/if}

    <!-- clickable hint arrow -->
    <span class="click-arrow" aria-hidden="true">→ → →</span>
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
    position: relative; /* ✅ needed for overlay */
  }

  .image {
    width: 100%;
    height: 100%;
    object-fit: cover;
    display: block;
  }

  .click-arrow {
    font-family: var(--font-mono);
    position: absolute;
    right: 12px;
    bottom: 8px;    
    line-height: 1;
    pointer-events: none; /* don’t block clicking */
    color: var(--color-highlight);
    /* font-family intentionally not set here (uses inherited/body font) */
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
