<script lang="ts">
    export let chapter: string = "";
</script>

<div class="introduction">
    <div class="divider"></div>
    <div class="chapter-intro">{chapter}</div>
</div>

<style>
    .introduction {
        display: flex;
        flex-direction: column;
        gap: 4px;
    }

    .divider {
        width: 100%;
        height: 0; 
        border-top: 1px dashed var(--color-highlight);
    }

    @media (min-width: 900px) {
        .introduction {
            gap: 6px;
        }
    }
</style>
