<script>
	async function getRandomNumber() {
		let res = await fetch('/');
		let text = await res.text();
		if ( res.ok ) {
			return Math.random();
		}
		else {
			throw new Error(text);
		}
	}

	let promise = getRandomNumber();

	function onClick(e) {
		promise = getRandomNumber();
	}
</script>

<h3>Promise</h3>

<button on:click={onClick}>Get Random Number</button>

<p>Random number: 
{#await promise}
	fetching...
{:then number}
	{number}
{:catch err}
	{err.message}
{/await}
</p>
