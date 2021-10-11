<script>
	let html = '<p>Some text</p>';
</script>

<p>html = "{html}"</p>
<div contenteditable="true" bind:textContent={html}></div>
<div contenteditable="true" bind:innerHTML={html}></div>
