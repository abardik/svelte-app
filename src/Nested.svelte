<style>
	p {
		color: red;
	}
</style>

<script>
	export let title, text; // or use $$props.title
	$: str = 'Some <b>bold</b> text. ' + text;
</script>

<p>Nested paragraph. {@html str} Another {@html '<b>bold</b> text'}</p>
<p>Answer: {$$props.answer}</p>
<p>Title: {title}</p>
