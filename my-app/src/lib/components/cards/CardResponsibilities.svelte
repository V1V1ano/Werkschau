<script lang="ts">
    import KeyArea from "$lib/components/KeyArea.svelte";
    type KeyAreaVariant = "ui" | "conceptual" | "narratives" | "speculative";

    export let text: string;
    export let keyArea: KeyAreaVariant;
</script>

<div class="card">
    <div class="key-areas-description">{text}</div>
    <div class="keyarea-wrapper"><KeyArea variant={keyArea} /></div>
</div>

<style>
    .card {
        display: flex;
        flex-direction: column;
        gap: 28px;
        padding: 10px;
        border: 1px dashed var(--color-primary);
        align-items: flex-end;
    }

    .key-areas-description {
        width: 100%; /* fills width */
        flex: 1;
    }

    @media (min-width: 900px) {
       .card {
        gap: 48px;
        padding: 18px;
       } 
    }
</style>
