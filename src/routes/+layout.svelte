<script>
	import '../app.css';
	import { onMount } from 'svelte';

	let Ads;
	onMount(async () => {
		Ads = (await import('../components/GoogleAds.svelte')).default;
	});
</script>

<slot />
<svelte:component this={Ads} />
