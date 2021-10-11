<style>
	div {
		display: inline-block;
	}
</style>

<script>
	let w, h, size = 20, text = 'Some Text';

</script>

<input type="range" bind:value={size} min=0 max=100/>
<input type="text" bind:value={text}/>
<p>Width: {w}px Height: {h}px</p>
<div bind:clientWidth={w} bind:clientHeight={h}><span style="font-size: {size}px">{text}</span></div>
