<script>
	export let item;
</script>

{#if item === 'error'}
	<div class="error-cont">
		<h1 class="error-text">
			Hmm... We cannot access this URL. <br />
			<span>Either the URL is incorrect, or our services may be down.</span>
		</h1>
	</div>
{:else}
	<div class="container">
		<a class="title" target="_blank" href={item.link}>{item.title}</a>
		<p class="origin">{item.displayLink}</p>
		<!-- <p id="readtime0" class="readtime"></p> -->
	</div>
{/if}

<style>
	@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@200;400&display=swap');
	@import url('https://fonts.googleapis.com/css2?family=Darker+Grotesque:wght@600&display=swap');
	@import url('https://fonts.googleapis.com/css2?family=Darker+Grotesque:wght@600&family=Rubik+Iso&display=swap');
	@import url('https://fonts.googleapis.com/css2?family=Varela+Round&display=swap');
	@import url('https://fonts.googleapis.com/css2?family=Press+Start+2P&family=Varela+Round&display=swap');
	.origin {
		position: absolute;
		font-family: 'Varela Round', sans-serif;
		bottom: 0px;
		left: 20px;
		font-size: 13px;
		padding-top: 5px;
	}
	.container {
		height: 75px;
		width: 90%;
		background-color: #ffebca;
		/* border: 1px solid burlywood; */
		box-shadow: 3px 4px 0px 1px #000;
		/* border-left: 0;
  border-right: 0; */
		border: 2px solid #000;

		padding: 12px 10px;
		border-radius: 4px;
		position: relative;
		overflow: hidden;
		margin-top: 10px;
		margin-bottom: 10px;
	}
	.title {
		font-size: 17px;
		position: relative;
		font-family: 'Varela Round', sans-serif;
		top: 10px;
		left: 10px;
		font-weight: bold;
		color: black;
		text-align: left;
		padding-top: 3px;
		overflow-y: hidden;
		word-wrap: break-word;
	}
	.error-text {
		font-family: 'Varela Round', sans-serif;
		font-size: 3vw;
		margin: auto;
	}
	.error-cont {
		display: flex;
		text-align: center;
		flex-direction: column;
		align-items: center;
		width: 80%;
		padding: 19px 10px;
		padding-top: 30px;
		justify-content: center;
	}
</style>
