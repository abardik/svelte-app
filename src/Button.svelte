<style>
	button {
		text-transform: uppercase;
	}
</style>

<script>
	let count = 0;
	$: doubled = count * 2;
	$: console.log(count, doubled);
	function onClick(e) {
		++count;
	}
	$: {
		if ( count > 5 ) {
			count = 0;
			alert('Danger!');
		}
	}
</script>

<button on:click={onClick}>Clicked {count} time{count==1 ? '' : 's'}</button>
<!--<button on:click={() => ++count}>Clicked {count} time{count==1 ? '' : 's'}</button>-->

<span>(doubled = {doubled})</span>
