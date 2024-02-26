<script>
	import { weapons } from '$lib/weapons';
	import { weaponCard } from '../components';
	import { swordAndShieldValues } from '$lib/weaponValues/swordAndShieldValues';
	import WeaponCard from '../components/weaponCard.svelte';
	let weapon = '';
	let weaponType = {};
	console.log('what is weapon', weaponType);
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
		You selected: {weapon}
	</p>
	{#if weapon}
		<div class={'m-5 p-5 rounded-xl bg-[#E5D7B7] text-2xl font-bold'}>
			<option value={''}>Select A Weapon Type</option>
			{#each swordAndShieldValues as swordAndShieldValue}
				{#if weapon === 'Sword and Shield'}
					<WeaponCard
						class={'m-5 p-5 rounded-xl bg-[#E5D7B7] border-4 border-[#3B2E25]'}
						weapon={swordAndShieldValue}
						on:click={() => {
							weaponType = swordAndShieldValue.name;
						}}
					/>
					<!-- <option value={swordAndShieldValue.name}>{swordAndShieldValue.name}</option> -->
				{/if}
			{/each}
		</div>
		<p class={'text-2xl font-bold text-white'}>
			You selected: {weaponType}
		</p>
	{/if}
</div>

<h1 class={'flex font-bold'}>Welcome to SvelteKit! For real!.</h1>
<p>Visit <a href="https://kit.svelte.dev">kit.svelte.dev</a> to read the documentation</p>

<style lang="postcss">
	:global(html) {
		background-image: url('https://images.unsplash.com/photo-1635200487290-f91d14f64bd3?q=80&w=2488&auto=format&fit=crop&ixlib=rb-4.0.3&ixid=M3wxMjA3fDB8MHxwaG90by1wYWdlfHx8fGVufDB8fHx8fA%3D%3D');
	}
</style>
