<script lang="ts">
    import { onMount } from "svelte";
    import ButtonAction from "$lib/components/Buttons/ButtonAction.svelte";

    export let headline: string = "title";
    export let buttonLabel: string = "label";
    export let items: string[] = ["a", "b", "c", "d"];

    export let prefix: string = "→ ";

    let index = 0;

    function shuffle() {
        if (items.length <= 1) return;
        let next = index;
        while (next === index) next = Math.floor(Math.random() * items.length);
        index = next;
    }

    onMount(() => {
        if (items.length > 1) index = Math.floor(Math.random() * items.length);
    });
</script>

<div class="milestone">
    <div class="body">{headline}</div>
    <ButtonAction type="internal" on:click={shuffle}>
        {buttonLabel}
    </ButtonAction>
    <div class="sub-headline">{prefix}{items[index]}</div>
</div>

<style>
    .milestone {
        display: flex;
        flex-direction: column;
        gap: 18px;
    }

    .sub-headline {
        color: var(--color-highlight);
    }
</style>
