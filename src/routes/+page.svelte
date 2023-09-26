<script>
	import Article from './article.svelte';
	import Navbar from './navbar.svelte';
	import Adblock from './adblock.svelte';
	import Ad1 from './ad1.svelte';
	import DisableAdblock from './disable-adblock.svelte';
	import { onMount } from 'svelte';
	import FlyUp from './fly-up.svelte';
	import TopBanner from './top-banner.svelte';
	import FlyDown from './fly-down.svelte';
	import Newsletter from './newsletter.svelte';

	onMount(() => {});

	let showAd1 = false;
	let showAdblock = false;
	let showDisableAdblock = false;
	let showTopBanner = false;
	let showNewsletter = false;
	setTimeout(() => {
		showAdblock = true;
		setTimeout(() => {
			enableAd1();
		}, 2000);
	}, 2000);
	const closeAdBlock = () => {
		showAdblock = false;
	};
	const onDisableAdblock = () => {
		closeAdBlock();
		showDisableAdblock = true;
	};
	const closeDisableAdblock = () => {
		showDisableAdblock = false;
	};
	const enableAd1 = () => {
		showAd1 = true;
		setTimeout(() => {
			enableTopBanner();
		}, 3000);
	};
	const enableTopBanner = () => {
		showTopBanner = true;
		setTimout(() => {
			enableNewsletter();
		}, 2000);
	};
	const closeTopBanner = () => {
		showTopBanner = false;
	};
	const enableNewsletter = () => {
		showNewsletter = true;
	};
</script>

{#if showNewsletter}
	<FlyUp>
		<Newsletter />
	</FlyUp>
{/if}

{#if showAdblock}
	<FlyUp>
		<Adblock id="adblock" close={closeAdBlock} more={onDisableAdblock} />
	</FlyUp>
{/if}
{#if showDisableAdblock}
	<FlyUp>
		<DisableAdblock close={closeDisableAdblock} />
	</FlyUp>
{/if}
{#if showAd1}
	<FlyUp>
		<Ad1 />
	</FlyUp>
{/if}
{#if showTopBanner}
	<FlyDown>
		<TopBanner close={closeTopBanner} />
	</FlyDown>
{/if}
<Navbar />
<main>
	<Article />
</main>
