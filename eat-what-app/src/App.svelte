<script>
	import Header from "./components/Header.svelte";
	import CardContainer from "./components/CardContainer.svelte"
</script>

<div class="nes">
	<!-- <Header /> -->
	<main>
		<img
			src="https://img.icons8.com/color/48/000000/jelly.png"
			alt="Steak"
			class="nes-avatar is-rounded is-large"
			style="image-rendering: pixelated;"
		/>
		<section class="blank">一般人看不到这一行</section>
		<CardContainer></CardContainer>
	</main>
</div>

<style>
	@font-face {
		font-family: "zpix";
		src: url("./zpix-v1.2.1-legacy.ttf");
	}
	.nes {
		font-family: "zpix";
		color: rgb(33, 37, 41);
	}
	.blank {
		height: 5em;
	}

	/* @media (min-width: 640px) {
	} */
</style>
