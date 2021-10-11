<script>
	let todos = [
		{ done: false, text: 'todo 1' },
		{ done: false, text: 'todo 2' },
		{ done: false, text: 'todo 3' },
		{ done: false, text: 'todo 4' },
		{ done: false, text: 'todo 5' },
	];
	function add() {
		todos = todos.concat({ done: false, text: '' });
	}
	function clear() {
		todos = todos.filter(t => ! t.done);
	}
	$: undone = todos.filter(t => ! t.done).length;
	$: console.log(todos);
</script>

{#each todos as todo}
	<div class:done={todo.done}>
		<input type="checkbox" bind:checked={todo.done}/>
		<input type="text" bind:value={todo.text}/>
	</div>
{/each}

<p>Undone: {undone}</p>
<button on:click={add}>Add</button>
<button on:click={clear}>Clear</button>
