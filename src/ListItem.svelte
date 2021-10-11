<script>
	const icons = {
		apple: '🍎',
		banana: '🍌',
		carrot: '🥕',
		doughnut: '🍩',
		egg: '🥚',
	};
	export let i, item;
	//export let {i, item} = $$props; // the same
</script>

<li>{++i}. <a id={item.id} href={item.url}>{item.name}</a> <span>{icons[item.name]}</span></li>
