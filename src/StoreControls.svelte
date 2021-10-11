<script>
	import {count, smartCount} from './store.js';

	function increment() {
		count.update(num => num + 1);
	}
	function decrement() {
		count.update(num => num - 1);
	}
	function reset() {
		count.set(0);
	}
</script>

<button on:click={increment}>+</button>
<button on:click={decrement}>-</button>
<button on:click={reset}>0</button>

<p>Count: {$count}</p>
<!-- use $ to get value of Store variables -->

<hr/>

<button on:click={smartCount.increment}>+</button>
<button on:click={smartCount.decrement}>-</button>
<button on:click={smartCount.reset}>0</button>

<p>Count: {$smartCount}</p>
