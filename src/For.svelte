<script>
	let cats = [
		{ id: 'J---aiyznGQ', name: 'Keyboard Cat' },
		{ id: 'z_AbfPXTKms', name: 'Maru' },
		{ id: 'OUtn3pvWmpg', name: 'Henri The Existential Cat' }
	];

	import Thing from './Thing.svelte';

	let things = [
		{ id: 1, value: 'a' },
		{ id: 2, value: 'b' },
		{ id: 3, value: 'c' },
		{ id: 4, value: 'd' },
		{ id: 5, value: 'e' }
	];

	function handleClick() {
		things = things.slice(1);
	}
</script>


<p>example 1</p>
<ul>
	{#each cats as cat, i}
		<li><a target="_blank" href="https://www.youtube.com/watch?v={cat.id}">
			{i + 1}: name is {cat.name}
		</a></li>
	{/each}
</ul>


<p>examlpe 2</p>
<ul>
	{#each cats as {name, id}, i}
		<li><a target="_blank" href="https://www.youtube.com/watch?v={id}">
			{i + 1}: name is {name}
		</a></li>
	{/each}
</ul>


<p>example 3</p>

<button on:click={handleClick}>
	Remove first thing
</button>

{#each things as thing}
	<Thing value={thing.value}/>
{/each}