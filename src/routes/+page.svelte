<script>
	import Article from './article.svelte';
	import Navbar from './navbar.svelte';
	import Adblock from './adblock.svelte';
	import Ad1 from './ad1.svelte';
	import DisableAdblock from './disable-adblock.svelte';
	import { onMount } from 'svelte';

	onMount(() => {});

	let showAd1 = false;
	let showAdblock = false;
	let showDisableAdblock = false;
	setTimeout(() => {
		showAdblock = true;
	}, 2000);
	const closeAdBlock = () => {
		showAdblock = false;
		setTimeout(() => {
			showAd1 = true;
		}, 2000);
	};
	const onDisableAdblock = () => {
		closeAdBlock();
		showDisableAdblock = true;
	};
	const closeDisableAdblock = () => {
		showDisableAdblock = false;
	};
</script>

{#if showAdblock}
	<Adblock id="adblock" close={closeAdBlock} more={onDisableAdblock} />
{/if}
{#if showDisableAdblock}
	<DisableAdblock close={closeDisableAdblock} />
{/if}
{#if showAd1}
	<Ad1 />
{/if}
<Navbar />
<main>
	<Article />
</main>

<style>
	@keyframes fadeIn {
		0% {
			opacity: 0%;
		}
		100% {
			opacity: 100%;
		}
	}
	@keyframes fadeOut {
		0% {
			opacity: 100%;
		}
		100% {
			opacity: 0%;
		}
	}
</style>
