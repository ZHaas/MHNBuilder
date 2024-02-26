<script>
	export let weapon = {
		name: 'Iron',
		skill: 'Poison Resistance',
		skillValue: '2',
		maxPower: '1596',
		affinity: '0',
		element: 'none',
		elementPower: '0'
	};
	let props = { ...$$restProps };
</script>

<button class={props.class} style={props.style} on:click>
	<h3>{weapon.name}</h3>
	<p>{weapon.skill}</p>
	<p>{weapon.skillValue}</p>
	<p>{weapon.maxPower}</p>
	<p>{weapon.affinity}</p>
	<p>{weapon.element}</p>
	<p>{weapon.elementPower}</p>
	<slot />
</button>
