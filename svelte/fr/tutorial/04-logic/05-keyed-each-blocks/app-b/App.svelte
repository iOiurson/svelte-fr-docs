<script>
	import Thing from './Thing.svelte';

	let things = [
		{ id: 1, name: 'pomme' },
		{ id: 2, name: 'banane' },
		{ id: 3, name: 'carotte' },
		{ id: 4, name: 'donut' },
		{ id: 5, name: 'oeuf' },
	];

	function handleClick() {
		things = things.slice(1);
	}
</script>

<button on:click={handleClick}>
	Supprimer le premier élément
</button>

<div style="display: grid; grid-template-columns: 1fr 1fr; grid-gap: 1em">
	<div>
		<h2>Avec clé</h2>
		{#each things as thing (thing.id)}
			<Thing current={thing.color}/>
		{/each}
	</div>

	<div>
		<h2>Sans clé</h2>
		{#each things as thing}
			<Thing current={thing.color}/>
		{/each}
	</div>
</div>
