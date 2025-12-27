<script>
  import NavAbout from "$lib/components/nav/NavAbout.svelte";
</script>

<div class="outer-gaps">
  <NavAbout />

  <main>
    <slot />
  </main>
</div>

<style>
  .outer-gaps {
    display: flex;
    flex-direction: column;
    gap: 48px;
    margin-bottom: 48px;
  }

  @media (min-width: 900px) {
    .outer-gaps {
      gap: 64px;
      margin-bottom: 96px;
    }
  }
</style>
