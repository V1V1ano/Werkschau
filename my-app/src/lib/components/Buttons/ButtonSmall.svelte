<script lang="ts">
  export let href: string = '#';
  export let type: 'external' | 'internal' = 'internal';
  $: arrow = type === 'external' ? '↗' : '→';
</script>

<a class="button-small" href={href}>
  <span class="label">
    <slot />
  </span>
  <span class="arrow" aria-hidden="true">{arrow}</span>
</a>

<style>
  .button-small {
    display: flex;
    justify-content: flex-start; /* content justified right */
    gap: 12px;          /* mobile */
    color: var(--color-highlight);
    background: transparent;
    text-decoration: none;
  }

  /* buttons are always "hover color" */
  .button-small:hover {
    color: var(--color-primary);
  }
</style>
