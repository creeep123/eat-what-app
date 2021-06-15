<script>
	import Header from "./components/Header.svelte";
	import CardContainer from "./components/CardContainer.svelte";
</script>

<div class="root">
	<div class="nes">
		<!-- <Header /> -->
		<main>
			<!-- <img
				src="https://img.icons8.com/color/48/000000/jelly.png"
				alt="Steak"
				class="nes-avatar is-rounded is-large"
				style="image-rendering: pixelated;"
			/>
			<section class="blank">一般人看不到这一行</section> -->
			<CardContainer />
		</main>
	</div>
</div>

<style>
	* {
		margin: 0;
		padding: 0;
	}
	@font-face {
		font-family: "zpix";
		src: url("./fonts/zpix-v1.2.1-legacy.ttf");
	}
	.root{
		display: flex;
		justify-content: center;
		width: 100%;
	}
	.nes {
		font-family: "zpix";
		color: rgb(33, 37, 41);
		min-width: 600px;
		/* width: 80%; */
	}
	.blank {
		height: 5em;
	}

	/* @media (min-width: 640px) {
	} */
</style>
