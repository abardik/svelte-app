<script>
	let user = { loggedIn: false };
	function onClick(e) {
		user.loggedIn = ! user.loggedIn;
	}
</script>

<button on:click={onClick}>{#if user.loggedIn}Log Out{:else}Log In{/if}</button>
