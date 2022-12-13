<script>
	import Button from './components/Button.svelte';
	import Counter from './components/Counter.svelte';

  let click = 0;

	const counterClick = () => {
		click += 1;
	};

	const restartCounter = () => {
		click = 0;
	};
</script>

<div class="main-container">
	<div class="container-logo">
		<img
			class='logo'
			src='./images/freeCodeCampLogo.jpg'
			alt='logo of page'
		/>
	</div>
	<div class="container-counter">
		<Counter
			text={click}
		/>
		<Button 
			text='Click'
			manageClick={counterClick}
		/>
		<Button 
			text='Restart'
			manageClick={restartCounter}
		/>
	</div>
</div>

<style>
	:global(body) {
		background-color: #000000;
	}
	
	.main-container {
		display: flex;
		flex-wrap: wrap;
		align-items: center;
		justify-content: center;
		padding-top: 15px;
		font-family: Lato, sans-serif;
	}
	
	.container-logo {
		width: 100%;
		display: flex;
		align-items: center;
		justify-content: center;
		margin: 10px
	}
	
	.logo {
		height: 50px;
	}
	
	.container-counter {
		width: min-content;
	}
</style>
