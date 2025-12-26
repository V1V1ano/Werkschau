<script lang="ts">
    import Button from "$lib/components/Buttons/Button.svelte";

    export let from: string;
    export let to: string | null = null;

    export let title: string;
    export let place: string;

    export let logoSrc: string;

    // optional link
    export let linkHref: string | null = null;
    export let linkLabel: string = "Author Profile ↗";
    export let linkType: "internal" | "external" = "external";
</script>

<div class="card-cv">
    <div class="top">
        <div class="table-label">
            {from}
            {#if to}
                –&nbsp;{to}
            {/if}
        </div>

        {#if linkHref}
            <div class="card-cv-link">
                <Button href={linkHref} type={linkType}>
                    {linkLabel}
                </Button>
            </div>
        {/if}
    </div>

    <div class="divider"></div>

    <div class="bottom">
        <div class="card-cv-logo">
            <img src={logoSrc} loading="lazy" />
        </div>

        <div class="card-cv-meta">
            <div class="table-value">{title}</div>
            <div class="table-value">{place}</div>
        </div>
    </div>
</div>

<style>
    .card-cv {
        border: 1px dashed;
        padding: 10px;
        display: flex;
        flex-direction: column;
        gap: 10px;
    }

    .card-cv .top {
        display: flex;
        gap: 28px;
        justify-content: space-between;
        align-items: end;
    }

    .card-cv .bottom {
        display: flex;
        gap: 28px;
    }

    .card-cv-link {
        width: calc(70% - 28px);
    }

    .card-cv-logo {
        max-width: 30%;
    }

    .card-cv-logo img {
        width: 100%;
        height: auto;
        display: block;
        object-fit: contain;
    }

    .card-cv :global(.button-main) {
        min-width: 0px;
    }

    .divider {
        height: 1px;
        background: var(--color-primary);
    }

    @media (min-width: 900px) {
        .card-cv {
            padding: 14px;
        }
    }
</style>
