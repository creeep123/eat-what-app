<script>
    let foods = [
        {
            icon:
                "https://img.icons8.com/color/48/000000/pizza-five-eighths.png",
            name: "pizza",
        },
        { icon: "", name: "2" },
        { icon: "", name: "3" },
        { icon: "", name: "4" },
        { icon: "", name: "5" },
        { icon: "", name: "6" },
        { icon: "", name: "7" },
        { icon: "", name: "8" },
        { icon: "", name: "9" },
    ];
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
        height:100%;
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
