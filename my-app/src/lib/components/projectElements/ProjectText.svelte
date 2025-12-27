<script lang="ts">
    import Button from "../Buttons/Button.svelte";

    // optional content parts
    export let body: string | null = null;
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
        <div class="big-text-wrapper">
            <div class="highlight-text">{highlight}</div>
        </div>
    {/if}

    {#if body}
        <div class="body">{body}</div>
    {/if}

    {#if linkHref && linkLabel}
        <Button href={linkHref} type="external">{linkLabel}</Button>
    {/if}
</div>

<style>
    .project-text {
        display: flex;
        flex-direction: column;
        gap: 12px;
    }

    .big-text-wrapper {
        margin-bottom: 32px;
    }

    .quote {
        margin:  0 0 32px 0;
        display: flex;
        flex-direction: column;
        gap: 8px;
    }
</style>
