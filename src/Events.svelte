<style>
	div {
		background-color: silver;
		width: 300px;
		height: 200px;
		display: inline-flex;
		align-items: center;
		justify-content: center;
	}
</style>

<script>
	let m = { x: 0, y: 0 };
	function onMousemove(e) {
		m.x = e.clientX;
		m.y = e.clientY;
	}
	function onClick(e) {
		alert('Click');
	}

	import { createEventDispatcher } from 'svelte';
	const dispatch = createEventDispatcher();

	function dispatchEvent(e) {
		dispatch('message', { text: 'Hello!' });
	}
</script>

<!-- modifiers: preventDefault|stopPropagation|passive|nonpassive|capture|once|self|trusted -->

<div on:mousemove={onMousemove} on:click|once={onClick}>
	<p>X: {m.x} Y: {m.y}</p>
</div>

<button on:click={dispatchEvent}>Dispatch Event</button>

<button on:click>Forward Event</button>
<!-- event without handler forwards to parent component -->
<!-- on:message without handler forwards all 'message' events to parent component -->
