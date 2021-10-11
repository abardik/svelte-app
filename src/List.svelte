<script>
	import ListItem from './ListItem.svelte';
	let items = [
		{ id: '11111', name: 'apple', url: '/apple' },
		{ id: '22222', name: 'banana', url: '/banana' },
		{ id: '33333', name: 'carrot', url: '/carrot' },
		{ id: '44444', name: 'doughnut', url: '/doughnut' },
		{ id: '55555', name: 'egg', url: '/egg' },
	];
	const icons = {
		apple: '🍎',
		banana: '🍌',
		carrot: '🥕',
		doughnut: '🍩',
		egg: '🥚',
	};
	function onClick() {
		items = items.slice(1);
	}
</script>

<h3>List</h3>

<button on:click={onClick}>Remove First Item</button>

<ul>
	{#each items as item, i (item.id)}
		<ListItem {i} {item}/>
	{/each}
</ul>
