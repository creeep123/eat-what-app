<script>
  import Header from './components/Header.svelte';
  import CardContainer from './components/CardContainer.svelte';
</script>

<div class="root">
  <div class="nes">
    <!-- <Header /> -->
    <main>
      <section class="title">
        <h1>¿ 吃什么 ?</h1>
        <div>
          <img
            src="https://gitee.com/yxon123/gitee-sources/raw/master//Images/food-blogger.png"
            alt="Steak"
            class="nes-avatar is-rounded is-large"
            style="image-rendering: pixelated;"
          />
        </div>
      </section>
      <CardContainer />
    </main>
  </div>
</div>

<style>
  :global(body) {
    background: url('./assets/philipp-a-urlich-oldtree-640x320-1b.jpg');
  }
  @media screen and (max-width: 2100px) {
    .nes {
      width: 540px;
    }
  }
  @media screen and (max-width: 600px) {
    .nes {
      width: 360px;
    }
  }
  @font-face {
    font-family: 'zpix';
    src: url('./fonts/zpix-v1.2.1-legacy.ttf');
  }
  .root {
    display: flex;
    justify-content: center;
    /* width: 100%; */
  }
  .nes {
    font-family: 'zpix';
    color: rgb(33, 37, 41);
  }
  .title {
    display: flex;
    flex-direction: column;
    justify-content: center;
    align-items: center;
    margin-top: 20px;
    margin-bottom: 20px;
  }

  /* @media (min-width: 640px) {
	} */
</style>
