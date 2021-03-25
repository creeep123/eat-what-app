<script>
    let foods = [
        { icon: "", name: "1" },
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
                    {i} Good morning. Thou hast had a good night's sleep, I hope.
                </p>
            </div>
        {/each}
    </div>
</div>

<style>
    @media screen and (min-width: 600px) {
        .foodSquare {
            font-size: 24px;
        }
    }
    .grid {
        display: grid;
        /* grid-template-columns: repeat(3,1fr);
        grid-template-rows:repeat(3,1fr); */
        grid-template-columns:  repeat(3, 33.33%) ;
        grid-template-rows:  repeat(3, 33.33%) ;
        grid-gap: 1%;
        grid-auto-flow: row;
    }
</style>
