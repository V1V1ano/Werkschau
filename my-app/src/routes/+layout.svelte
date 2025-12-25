<script lang="ts">
	import favicon from "$lib/assets/favicon.svg";
	import Footer from "$lib/components/Footer.svelte";
	import "../app.css";
	let { children } = $props();
</script>

<svelte:head>
	<link rel="icon" href={favicon} />
</svelte:head>

<main class="page">
	{@render children()}
</main>

<Footer />

<style>
	/* Page padding */
	.page {
		padding-bottom: 16px;
		padding-left: 16px;
		padding-right: 16px; /* mobile */
	}

	@media (min-width: 900px) {
		.page {
			padding: 24px; /* desktop */
		}
	}
</style>
