<script lang="ts">
    import Button from "../Buttons/Button.svelte";

    // optional content parts
    export let body: string | string[] | null = null;
    export let highlight: string | null = null;

    // optional quote + source
    export let quote: string | null = null;
    export let quoteSource: string | null = null;

    // optional link (simple for now)
    export let linkLabel: string | null = null;
    export let linkHref: string | null = null;
</script>

<div class="project-text">
    {#if quote}
        <blockquote class="quote">
            <div class="highlight-text">“{quote}”</div>
            {#if quoteSource}
                <div class="caption">{quoteSource}</div>
            {/if}
        </blockquote>
    {/if}

    {#if highlight}
        <div class="margin-wrapper">
            <div class="highlight-text">{highlight}</div>
        </div>
    {/if}

    {#if body}
        <!-- <div class="margin-wrapper"> -->
        {#if Array.isArray(body)}
            {#each body as paragraph}
                <div class="body">{paragraph}</div>
            {/each}
        {:else}
            <div class="body">{body}</div>
        {/if}
        <!-- </div> -->
    {/if}

    {#if linkHref && linkLabel}
        <div class="margin-top-wrapper">
            <div class="button-wrap">
                <Button href={linkHref} type="external">{linkLabel}</Button>
            </div>
        </div>
    {/if}
</div>

<style>
    .project-text {
        display: flex;
        flex-direction: column;
        gap: 16px;
    }

    .margin-wrapper {
        display: flex;
        flex-direction: column;
        gap: 16px;
        margin-bottom: 32px;
    }

    .margin-top-wrapper {
        display: flex;
        flex-direction: column;
        margin-top: 32px;
    }

    .quote {
        margin: 0 0 32px 0;
        display: flex;
        flex-direction: column;
        gap: 16px;
    }

    .button-wrap {
        display: flex; /* so we can justify */
        align-self: flex-end;
    }

    @media (min-width: 900px) {
        .button-wrap :global(.button-main) {
            min-width: 0;
        }

        .margin-wrapper {
            margin-bottom: 40px;
        }

        .margin-top-wrapper {
            margin-bottom: 40px;
        }

        .project-text {
            gap: 16px;
        }

        .quote {
            gap: 12px;
        }
    }
</style>
