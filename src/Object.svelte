<script>
	let obj1 = { param1: 'value1', param2: 'value2' };
	$: obj2 = obj1.param1;
	$: console.log(obj1, obj2);
	function onClick(e) {
		obj2 = 'none'; // obj1.param1 = 'value1'
		obj1.param1 = '111'; // obj2 = '111'
	}
</script>

<button on:click={onClick}>Change Object</button>
