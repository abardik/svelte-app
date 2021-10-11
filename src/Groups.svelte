<script>
	let menu = [
		'item 1',
		'item 2',
		'item 3',
		'item 4',
		'item 5',
	];
</script>

{#each menu as item}
	<label><input type="checkbox" bind:group={menu} name="group" value={item}/> {item}</label>
{/each}
