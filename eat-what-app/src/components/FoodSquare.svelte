<script>
    export let foods
</script>

<div class="foodSquare">
    <div class="grid">
        {#each foods as food, i}
            <div class="nes-container is-dark with-title">
                <p class="title">{food.name}</p>
                <p>
                    <img
                        src={food.icon}
                        alt={food.name}
                        class="nes-avatar is-rounded is-large"
                        style="image-rendering: pixelated;"
                    />
                </p>
            </div>
        {/each}
    </div>
</div>

<style>
    .foodSquare {
        width:100%;
        /* height:100%; */
    }
    /* @media screen and (min-width: 960px) {
        .foodSquare {
            font-size: 24px;
        }
    } */
    .grid {
        display: grid;
        /* grid-template-columns: repeat(3,1fr);
        grid-template-rows:repeat(3,1fr); */
        grid-template-columns: repeat(3, 33.33%);
        grid-template-rows: repeat(3, 33.33%);
        grid-gap: 1%;
        grid-auto-flow: row;
    }
</style>
