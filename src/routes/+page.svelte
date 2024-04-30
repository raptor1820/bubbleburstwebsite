<script>
	import Card from './Card.svelte';
	let url = '';
	let data = [];

	async function handleClick() {
		if (!url.startsWith('https://') && !url.startsWith('http://')) {
			url = 'https://' + url;
		}
		await fetch('https://apibubbleburst.ritwic.com/?url=' + url).then(async (res) => {
			let x = await res.json();
			console.log(x);
			data = [];
			for (let item in x) {
				data = [...data, x[item]];
			}
			console.log(data);
		});
	}
</script>

<svelte:window on:keydown={(e) => e.key === 'Enter' && handleClick()} />
<div class="main-cont">
	<h1 class="main-header">BUBBLE BURST!</h1>
	<div class="input-cont">
		<input type="text" bind:value={url} class="textbox" />
		<button on:click={handleClick} class="submit-button">Go</button>
	</div>
	<h2 class="under-text">
		<i>Enter the URL of any news article and press GO to see the other side of the story...</i>
	</h2>
	{#each data as item}
		<Card {item} />
	{/each}
</div>

<style>
	@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@200;400&display=swap');
	@import url('https://fonts.googleapis.com/css2?family=Darker+Grotesque:wght@600&display=swap');
	@import url('https://fonts.googleapis.com/css2?family=Darker+Grotesque:wght@600&family=Rubik+Iso&display=swap');
	@import url('https://fonts.googleapis.com/css2?family=Varela+Round&display=swap');
	@import url('https://fonts.googleapis.com/css2?family=Press+Start+2P&family=Varela+Round&display=swap');
	:global(body) {
		background-color: #ffebca;
		scrollbar-color: black transparent;
		scrollbar-width: 10px;
	}
	:global(::-webkit-scrollbar) {
		width: 10px;
		background: transparent;
	}
	:global(::-webkit-scrollbar-thumb) {
		background: black;
		border-radius: 30px;
	}
	.main-header {
		font-family: 'Press Start 2P', cursive;
		font-size: 5vw;
	}
	.main-cont {
		display: flex;
		flex-direction: column;
		align-items: center;
	}
	.input-cont {
		width: 60vw;
		display: flex;
		flex-direction: row;
		justify-content: center;
		align-items: center;
	}
	.textbox {
		background-color: #ffebca;
		box-shadow: 3px 4px 0px 1px #000;
		border: 2px solid #000;
		height: 4rem;
		width: 60rem;
		overflow: hidden;
		outline: none;
		font-family: 'Varela Round', sans-serif;
		font-size: 2rem;
		overflow: hidden;
	}
	.textbox:hover,
	.textbox:focus {
		transform: translate(2px, 2px);
		box-shadow: 2px 2px 0px 0px;
	}
	.submit-button {
		padding: 0;
		margin: auto;
		background-color: #ffebca;
		box-shadow: 3px 4px 0px 1px #000;
		border: 2px solid #000;
		height: 4rem;
		width: 5rem;
		font-family: 'Varela Round', sans-serif;
		font-size: 2rem;
		outline: none;
		overflow: hidden;
	}
	.submit-button:hover {
		transform: translate(2px, 2px);
		cursor: pointer;
		box-shadow: 2px 2px 0px 0px;
	}
	.under-text {
		font-family: 'Varela Round', italic;
		font-size: 1.2vw;
		margin-top: 10px;
	}
	@media (max-width: 820px) {
		.textbox {
			width: 80rem;
			height: 2.5rem;
			font-size: 1.5rem;
		}
		.submit-button {
			height: 2.9rem;
			width: 20rem;
			font-size: 1.5rem;
		}
		.under-text {
			font-size: 3vw;
		}
	}
</style>
