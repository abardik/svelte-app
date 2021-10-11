<script>
	let name = 'Andy';
	let range = 3;
	let subscribe = false;
	$: fullName = 'Mr. ' + name;
	let value = 'Some text';

	let options = [
		{ id: 1, name: 'option 1' },
		{ id: 2, name: 'option 2' },
		{ id: 3, name: 'option 3' },
		{ id: 4, name: 'option 4' },
		{ id: 5, name: 'option 5' },
	];
	let selected = options[0];
	let multiSelected = [];
	$: console.log(selected);
	$: console.log(multiSelected);
</script>

<input type="text" bind:value={name}/>
<p>Full name: {fullName}</p>

<input type="number" bind:value={range} min=0 max=10/>
<input type="range" bind:value={range} min=0 max=10/>
<p>Range: {range}</p>

<label><input type="checkbox" bind:checked={subscribe}/> Yes, subscribe me to news and events</label>
<p>{#if subscribe}Thank you for your choice!{:else}Please, subscribe to our news and events.{/if}</p>
<button disabled={!subscribe}>Continue</button>

<br/>
<textarea bind:value></textarea>
<textarea bind:value={value}></textarea>

<br/>
<select bind:value={selected}>
	{#each options as option}
		<option value={option}>{option.name}</option>
	{/each}
</select>
<button on:click={e => selected = options[2]}>Select 3rd option</button>
<p>Selected: {selected.name}</p>

<select multiple bind:value={multiSelected}>
	{#each options as option}
		<option value={option}>{option.name}</option>
	{/each}
</select>

<form on:submit|preventDefault={e => alert('Hello!')}>
	<button type="submit">Submit</button>
</form>
