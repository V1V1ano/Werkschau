<script lang="ts">
    export let href: string; // e.g. /projects/werkschau
    export let title: string;
    export let context: string; // e.g. "Bachelor Thesis"
    export let year: string | number; // e.g. 2025
    export let imageSrc: string; // e.g. /previews/werkschau.png
</script>

<a class="preview" {href}>
    <div class="image-wrap">
        <img class="image" src={imageSrc} loading="lazy" />
    </div>

    <div class="divider"></div>

    <div class="info-grid">
        <div class="row">
            <div class="table-label">Project</div>
            <div class="table-value">
                {title}
            </div>
        </div>

        <div class="row">
            <div class="table-label">Context</div>
            <div class="table-value">
                {context}
            </div>
        </div>

        <div class="row">
            <div class="table-label">year</div>
            <div class="table-value">
                {year}
            </div>
        </div>
    </div>

    <div class="divider"></div>
</a>

<style>
    /* Layout only – no typography decisions */

    .preview {
        display: inline-flex;
        flex-direction: column;
        gap: 12px;
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
