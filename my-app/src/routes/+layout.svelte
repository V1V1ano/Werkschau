<script lang="ts">
	import favicon from '$lib/assets/favicon.svg';
	 import '../app.css';
	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

<main class="page">
  {@render children()}
</main>

<style>
  /* Page padding */
  .page {
    padding: 16px; /* mobile */
  }

  @media (min-width: 900px) {
    .page {
      padding: 24px; /* desktop */
    }
  }
</style>

