<script>
	import Header from "./components/Header.svelte";
</script>

<div class="nes">
	<Header />
	<img
		src="https://img.icons8.com/color/48/000000/jelly.png"
		alt="Steak"
		class="nes-avatar is-rounded is-large"
		style="image-rendering: pixelated;"
	/>
</div>

<style>
	@font-face {
		font-family: 'zpix';
		src: url('./fonts/zpix.ttf');
	}
	.nes {
		font-family: zpix;
	}

	@media (min-width: 640px) {
	}
</style>
