<script lang="ts">
  import { createEventDispatcher } from "svelte";

  export let type: "external" | "internal" = "internal";
  export let disabled: boolean = false;

  const dispatch = createEventDispatcher();
  $: arrow = type === "external" ? "↗" : "→";

  function handleClick(event: MouseEvent) {
    dispatch("click", event);
  }
</script>

<button
  class="button-main"
  type="button"
  disabled={disabled}
  on:click={handleClick}
>
  <span class="label">
    <slot />
  </span>
  <span class="arrow" aria-hidden="true">{arrow}</span>
</button>

<style>
  .button-main {
    display: flex;
    align-items: center;
    justify-content: flex-start;
    gap: 12px;

    padding: 8px;
    padding-left: 12px;
    border: 1px solid var(--color-highlight);

    color: var(--color-highlight);
    background: transparent;
    text-decoration: none;
    cursor: pointer;
  }

  .button-main:hover {
    background: var(--color-highlight);
    color: white;
  }

  .button-main:disabled {
    opacity: 0.5;
    cursor: not-allowed;
  }

  @media (min-width: 900px) {
    .button-main {
      padding: 14px 16px;
      max-width: 480px;
      min-width: 350px;
    }
  }
</style>
