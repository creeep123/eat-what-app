<script>
    // export let foods
    export let randomFood
</script>

<div class="controler">
    <div>
        <button type="button" class="nes-btn is-primary" on:click={randomFood}>随机一个</button>
    </div>
    <div>
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
    </div>
</div>

<style>
    .controler {
        margin-top: 18px;
        display: flex;
        flex-direction: column;
        justify-content: space-between;
        align-items: center;
        height: 160px;
    }
</style>