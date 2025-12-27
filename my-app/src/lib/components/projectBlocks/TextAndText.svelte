<script lang="ts">
  import Introduction from "../projectElements/Introduction.svelte";
  import ProjectText from "../projectElements/ProjectText.svelte";

  export let chapter: string;

  // left text meta
  export let leftBody: string | string[] | null = null;
  export let leftHighlight: string | null = null;
  export let leftQuote: string | null = null;
  export let leftQuoteSource: string | null = null;
  export let leftLinkLabel: string | null = null;
  export let leftLinkHref: string | null = null;

  // right text meta
  export let rightBody: string | string[] | null = null;
  export let rightHighlight: string | null = null;
  export let rightQuote: string | null = null;
  export let rightQuoteSource: string | null = null;
  export let rightLinkLabel: string | null = null;
  export let rightLinkHref: string | null = null;
</script>

<div class="text-and-text">
  <Introduction {chapter} />

  <div class="text-wrap">
    <ProjectText
      body={leftBody}
      highlight={leftHighlight}
      quote={leftQuote}
      quoteSource={leftQuoteSource}
      linkLabel={leftLinkLabel}
      linkHref={leftLinkHref}
    />

    <ProjectText
      body={rightBody}
      highlight={rightHighlight}
      quote={rightQuote}
      quoteSource={rightQuoteSource}
      linkLabel={rightLinkLabel}
      linkHref={rightLinkHref}
    />
  </div>
</div>

<style>
  .text-and-text {
    display: flex;
    flex-direction: column;
    gap: 18px;
  }

  .text-wrap {
    display: flex;
    flex-direction: column;
    gap: 12px;
  }

  @media (min-width: 900px) {
    .text-wrap {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      align-items: start;
      gap: 118px;
    }
  }
</style>
