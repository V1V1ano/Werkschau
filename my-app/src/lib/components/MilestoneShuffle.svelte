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
    <div class="shuffle-text">{prefix}{items[index]}</div>
</div>

<style>
    .milestone {
        display: flex;
        flex-direction: column;
        gap: 18px;
    }

    .shuffle-text {
        color: var(--color-highlight);
        font-family: var(--font-headline);
        font-size: 18px;
        letter-spacing: 0.2px;
    }

    @media (min-width: 900px) {
        .shuffle-text {
            font-size: 20px;
            line-height: 29px;
            letter-spacing: 0.3px;
        }
    }
</style>
