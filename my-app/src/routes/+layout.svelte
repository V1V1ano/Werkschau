<script lang="ts">
	import favicon from "$lib/assets/favicon.svg";
	import Footer from "$lib/components/Footer.svelte";
	import "../app.css";
	let { children } = $props();

	// Make text breaks prettier
	import { onMount } from "svelte";
	import { afterNavigate } from "$app/navigation";
	import balanceText from "balance-text";

	const selector = ".page .highlight-text, .page .body";

	function runBalance() {
		balanceText(document.querySelectorAll(selector));
	}

	onMount(() => {
		runBalance();

		const onResize = () => runBalance();
		window.addEventListener("resize", onResize);

		return () => window.removeEventListener("resize", onResize);
	});

	afterNavigate(() => {
		runBalance();
	});
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
			padding: 24px 48px;
		}
	}
</style>
