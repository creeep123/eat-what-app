<script>
  // export let foods
  export let randomFood;
  export let chance;
  let buttonState;
  let buttonText;
  $: buttonText = chance > 0 ? `随机` : `机会已用完`;
  $: buttonState = chance > 0 ? 'is-primary' : 'is-disabled';
</script>

<div class="controler">
  <div>
    <button
      type="button"
      class={`nes-btn ${buttonState}`}
      disabled={buttonState == 'is-disabled' ? true : false}
      on:click={randomFood}>{buttonText}</button
    >
  </div>
  <span class="chance-count">（剩余次数：{chance}）</span>
  <!-- <div>
        <label>
            <input type="checkbox" class="nes-checkbox" checked />
            <span>辣的</span>
        </label>
    </div>
    <div>
        <label>
            <input type="checkbox" class="nes-checkbox" checked />
            <span>贵的</span>
        </label>
    </div> -->
</div>

<style>
  .controler {
    margin-top: 18px;
    display: flex;
    flex-direction: column;
    justify-content: space-between;
    align-items: center;
    /* height: 160px; */
  }
  .chance-count {
    color: white;
  }
</style>
