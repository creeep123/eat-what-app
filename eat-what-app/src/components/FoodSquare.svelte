<script>
    // export let foods;
    export let showFoods;
</script>

<div class="foodSquare">
    <div class="grid">
        {#each showFoods as food, i}
            <div
                class="nes-container is-dark {food.rotate != undefined
                    ? ''
                    : 'with-title'} is-centered"
            >
                <p class="title">{food.name}</p>
                <p>
                    <img
                        src={food.icon}
                        alt={food.name}
                        class="{food.rotate != undefined
                            ? 'finger'
                            : 'foodImg'} nes-avatar is-rounded is-large"
                        style={`image-rendering: pixelated; transform:rotate(${food.rotate}deg);`}
                    />
                </p>
            </div>
        {/each}
    </div>
</div>

<style>
    @media screen and (max-width: 600px) {
        img{
            max-width: 32px;
            max-height: 32px;
        }
        p{
            font-size: 12px;
        }
    }
    /* @media screen and (min-width: 1601px) {
        .grid{
            width:480px;
            height:480px;
        }
    } */

    .grid {
        display: grid;
        grid-template-columns: repeat(3, 33.33%);
        grid-template-rows: repeat(3, 33.33%);
        grid-gap: 1%;
        grid-auto-flow: row;
    }

    @keyframes pop {
        0% {
            transform: scale(1, 1);
        }
        50% {
            transform: scale(1.3, 1.3) rotate(360deg);
        }
        100% {
            transform: scale(1, 1);
        }
    }

    .finger {
        transition: width, height 1s;
        animation: pop 1s;
    }
    .foodImg {
        transition: 1s;
    }
    .foodImg:hover {
        transform: scale(1.2, 1.2);
    }
</style>
