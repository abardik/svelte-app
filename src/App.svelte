<script>
	import Nested from './Nested.svelte';
	import Button from './Button.svelte';
	import Array from './Array.svelte';
	import Object from './Object.svelte';
	import Login from './Login.svelte';
	import List from './List.svelte';
	import Promise from './Promise.svelte';
	import Events from './Events.svelte';
	import Binding from './Binding.svelte';
	import Groups from './Groups.svelte';
	import Html from './Html.svelte';
	import Todo from './Todo.svelte';
	import Dimensions from './Dimensions.svelte';
	import BindProps from './BindProps.svelte';
	import BindThis from './BindThis.svelte';
	import OnMount from './OnMount.svelte';
	import Chat from './Chat.svelte';
	import Tick from './Tick.svelte';
	import Store from './Store.svelte';
	import ArrayIntegration from './ArrayIntegration.svelte';
	import TestComp from './TestComp.svelte';

	let prefix = 'Mr.';
	let name = 'Andy';
	$: title = prefix + ' ' + name;
	$: text = 'dear ' + title;
	$: obj = { title: title, text: text };
	let pin = '';
	$: view = pin ? pin : 'enter your pin';
	let field;
</script>

<!--
<h1 {title}>Hello, {text}!</h1>
<p>Root paragraph</p>
<Nested answer={42} {...obj}/>

<Button/>
<Array/>
<Object/>
<Login/>
<List/>
<Promise/>
<Events on:click={e => alert('Forwarded click')} on:message={e => alert(e.detail.text)}/>
<Groups/>
<Binding/>
<Html/>
<Todo/>
<Dimensions/>
<h1 style="color: {pin ? '#333' : '#ccc'}">{view}</h1>
<BindProps bind:value={pin} on:submit={e => alert(pin)}/>
<BindThis bind:this={field}/>
<button on:click={() => field.focus()}>Focus field</button>
<OnMount/>
<Chat/>
<Tick/>
<Store/>
<ArrayIntegration/>
<TestComp name="Andy"/>
-->
<Chat/>