<script lang="ts">
  import ProjectImage from "../projectElements/ProjectImage.svelte";

  // left image
  export let leftSrc: string;
  export let leftLabel: string | null = null;
  export let leftCredit: string | null = null;
  export let leftCaption: string | null = null;

  // right image
  export let rightSrc: string;
  export let rightLabel: string | null = null;
  export let rightCredit: string | null = null;
  export let rightCaption: string | null = null;
</script>

<div class="image-and-image">

  <div class="image-wrap">
    <ProjectImage
      src={leftSrc}
      label={leftLabel}
      credit={leftCredit}
      caption={leftCaption}
    />

    <ProjectImage
      src={rightSrc}
      label={rightLabel}
      credit={rightCredit}
      caption={rightCaption}
    />
  </div>
</div>

<style>
  .image-and-image {
    display: flex;
    flex-direction: column;
    gap: 18px;
  }

  .image-wrap {
    display: flex;
    flex-direction: column;
    gap: 18px;
  }

  @media (min-width: 900px) {
    .image-wrap {
      display: grid;
      grid-template-columns: repeat(2, minmax(0, 1fr));
      align-items: start;
      gap: 28px;
    }
  }
</style>
