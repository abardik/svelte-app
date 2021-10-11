<script>
	import {count, time, ellapsed, name, greeting} from './store.js';
	import StoreControls from './StoreControls.svelte';

	const formatter = new Intl.DateTimeFormat('en', {
		hour12: true,
		hour: 'numeric',
		minute: '2-digit',
		second: '2-digit'
	});
</script>

<p>Counter: {$count}</p>
<!-- use $ to get value of Store variables -->

<StoreControls/>

<h4>Time: {formatter.format($time)}</h4>

<p>Time on page: {$ellapsed} second{$ellapsed===1 ? '' : 's'}</p>

<h1>{$greeting}</h1>
<input bind:value={$name}/>
<button on:click={() => $name += '!'}>!</button>
