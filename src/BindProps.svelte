<style>
	.keypad {
		display: grid;
		grid-template-columns: repeat(3, 5em);
		grid-template-rows: repeat(4, 3em);
		grid-gap: 0.5em;
	}
	button {
		margin: 0;
	}
</style>

<script>
	import { createEventDispatcher } from 'svelte';
	const dispatch = createEventDispatcher();

	export let value = '';

	const select = (e) => value += e.target.innerText;
	const clear = () => value = '';
	const submit = () => dispatch('submit');
</script>

<div class="keypad">
	<button on:click={select}>1</button>
	<button on:click={select}>2</button>
	<button on:click={select}>3</button>
	<button on:click={select}>4</button>
	<button on:click={select}>5</button>
	<button on:click={select}>6</button>
	<button on:click={select}>7</button>
	<button on:click={select}>8</button>
	<button on:click={select}>9</button>
	<button disabled={!value} on:click={clear}>clear</button>
	<button on:click={select}>0</button>
	<button disabled={!value} on:click={submit}>submit</button>
</div>
