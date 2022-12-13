<script>
	export let text;
	export let manageClick;
</script>

<button 
	class={`button ${(text === 'Click') ? 'click' : 'restart'}`}
	on:click={manageClick}
>
	{text}
</button>

<style>
	.button {
		display: block;
		width: 280px;
		height: 84px;
		margin: 5px 0;
		border: 2px solid #ffffff;
		border-radius: 5px;
		font-size: 1.2rem;
		font-weight: 700;
		color: #ffffff;
		cursor: pointer;
	}
	
	.click {
		background-color: #45a897;
	}
	
	.click:hover {
		background-color: #4db09f;
	}
	
	.restart {
		background-color: #ac45b5;
	}
	
	.restart:hover {
		background-color: #b44dbd;
	}
</style>
