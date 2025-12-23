<script lang="ts">
  type KeyAreaVariant = "ui" | "conceptual" | "narratives" | "speculative";
  export let variant: KeyAreaVariant;

  const config: Record<KeyAreaVariant, { label: string; pattern: string }> = {
    ui: {
      label: "User Interfaces and Experiences",
      pattern: "/patterns/key-area-ui.png",
    },
    conceptual: {
      label: "Conceptual Data Vis Design",
      pattern: "/patterns/key-area-conceptual-vis.png",
    },
    narratives: {
      label: "Visual Narratives",
      pattern: "/patterns/key-area-narrative.png",
    },
    speculative: {
      label: "Speculative Software",
      pattern: "/patterns/key-area-speculative.png",
    },
  };

  $: label = config[variant].label;
  $: pattern = config[variant].pattern;
</script>

<div class="key-area">
  <div
    class="pattern"
    style:background-image={`url(${pattern})`}
    aria-hidden="true"
  ></div>

  <div class="key-areas-text">{label}</div>
</div>

<style>
  .key-area {
    display: inline-flex;
    align-items: center;
    gap: 8px;

    padding: 4px;
    padding-right: 10px;
    border: 1px solid var(--color-primary);

    /* prevents stretching in a parent flex column */
    align-self: flex-start;

    /* allows text to wrap once it hits the available width */
    max-width: 100%;
  }

  .pattern {
    width: 34px;
    height: 34px;
    background-size: contain;
    background-repeat: no-repeat;
    background-position: center;
  }
</style>
