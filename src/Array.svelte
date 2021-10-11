<script>
	let arr = [1, 2, 3, 4];
	$: sum = arr.reduce((t, n) => t + n, 0);
	$: console.log(arr, sum);
	function onClick(e) {
		arr[2] = 0; // reactive
		arr.push(arr.length + 1); // not reactive
		arr = arr; // to update after push/pop/shift/unshift
		//arr = arr.slice(1); // reactive
	}
</script>

<p>{arr.join(' + ')} = {sum}</p>

<button on:click={onClick}>Add Array</button>
