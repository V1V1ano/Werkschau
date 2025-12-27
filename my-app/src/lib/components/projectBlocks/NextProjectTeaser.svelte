<script lang="ts">
  import Button from "../Buttons/Button.svelte";

  export let href: string;
  export let src: string;
  export let tag: string | null = null;
</script>

<div class="next-project">
  <div class="inner">
    <div class="media">
      <img class="img" {src} loading="lazy" />

      <!-- overlay "bar button" -->
      <div class="top-overlay">
        <Button href={href} type="internal">Next Project</Button>
      </div>

      {#if tag}
        <div class="explanatory-tag">{tag}</div>
      {/if}
    </div>
  </div>
</div>

<style>
  .next-project {
    display: block;
  }

  .inner {
    border: 1px solid var(--color-highlight);
    width: 100%; /* ✅ important */
  }

  .media {
    position: relative;
    width: 100%;
    aspect-ratio: 1 / 1;
    overflow: hidden;
  }

  .img {
    width: 100%;
    height: 100%;
    object-fit: cover;
    display: block;
  }

  /* 🔑 overlay spans full width */
  .top-overlay {
    position: absolute;
    top: 0;
    left: 0;
    right: 0;          /* ✅ more reliable than width:100% */
    z-index: 2;
  }

  /* 🔑 force anchor-button to behave like a bar */
  .top-overlay :global(.button-main) {
    display: flex;     /* ✅ anchors are inline by default */
    width: 100%;
    box-sizing: border-box;

    max-width: none;
    min-width: 0;

    border-top: none;
    border-left: none;
    border-right: none;
    border-bottom: 1px solid var(--color-highlight);

    background: rgba(255, 255, 255, 0.8);
  }

  /* subtle hover, no CTA explosion */
  .top-overlay :global(.button-main:hover) {
    background-color: var(--color-highlight);
    color: white;
  }

  /* tag sits BELOW overlay bar */
  .explanatory-tag {
    position: absolute;
    left: 12px;
    top: 58px; /* aligns nicely under button */

    padding: 4px 10px;
    background-color: rgba(255, 255, 255, 0.6);
    border: 1px solid var(--color-primary);
    z-index: 3;
  }

  /* desktop: right column only */
  @media (min-width: 900px) {
    .next-project {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      gap: 28px;
      align-items: start;
    }

    .inner {
      grid-column: 2;
    }
  }
</style>
