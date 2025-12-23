<script lang="ts">
  export let href: string = '#';
  export let type: 'external' | 'internal' = 'internal';
  $: arrow = type === 'external' ? '↗' : '→';
</script>

<a class="button-main" href={href}>
  <span class="label">
    <slot />
  </span>
  <span class="arrow" aria-hidden="true">{arrow}</span>
</a>

<style>
  .button-main {
    display: flex;
    align-items: center;
    justify-content: flex-end; /* content justified right */
    gap: 12px;

    padding: 8px;            /* mobile */
    border: 1px solid var(--color-highlight);

    color: var(--color-highlight);
    background: transparent;
    text-decoration: none;
  }

  /* buttons are always "hover color" */
  .button-main:hover {
    background: var(--color-highlight);
    color: var(--color-primary);
  }

  @media (min-width: 900px) {
    .button-main {
      padding: 16px;          /* desktop */
    }
  }
</style>
