<script>
	import { weapons } from '$lib/weapons';
	let weapon = '';
	console.log('what is weapon', weapon);
</script>

<div
	class={'flex m-5 p-5 items-center justify-center rounded-xl bg-gradient-to-br from-orange-200 to-amber-700'}
>
	<p class={'text-white font-bold text-2xl text-center'}>
		Welcome to the Monster Hunter Now Kit Builder!
	</p>
</div>
<div
	class={'flex flex-col m-5 p-5 rounded-xl items-center justify-center bg-[#3B2E25] border-4 border-[#E5D7B7]'}
>
	<p class={'text-2xl font-bold text-white'}>Please select your weapon:</p>
	<select class={'m-5 p-5 rounded-xl bg-[#E5D7B7] text-2xl font-bold'} bind:value={weapon}>
		<option value={''}>Select A Weapon</option>
		{#each weapons as weapon}
			<option value={weapon.name}>{weapon.name}</option>
		{/each}
	</select>
	<p class={'text-2xl font-bold text-white'}>
		You selected: {weapon} More code being written check back soon
	</p>
	<!-- {#if weapon}
		<a
			href={`https://monsterhunternow.com/kit-builder?weapon=${weapon}`}
			class={'m-5 p-5 rounded-xl bg-[#E5D7B7] text-2xl font-bold'}
		>
			Build Your Kit
		</a>
	{/if} -->
</div>

<h1 class={'flex font-bold'}>Welcome to SvelteKit! For real!.</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>

<style lang="postcss">
	:global(html) {
		background-image: url('https://images.unsplash.com/photo-1635200487290-f91d14f64bd3?q=80&w=2488&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D');
	}
</style>
