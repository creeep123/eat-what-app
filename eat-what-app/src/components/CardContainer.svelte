<script>
  import FoodSquare from './FoodSquare.svelte';
  import Controler from './Controler.svelte';

  let foods = [
    {
      icon: 'https://img.icons8.com/color/48/000000/pizza-five-eighths.png',
      name: '披萨',
    },
    {
      icon: 'https://img.icons8.com/color/48/000000/paella.png',
      name: '香锅',
    },
    {
      icon: 'https://img.icons8.com/color/48/000000/hamburger.png',
      name: '汉堡',
    },
    {
      icon: 'https://img.icons8.com/color/48/000000/chicken.png',
      name: '炸鸡',
    },
    {
      icon: 'https://img.icons8.com/color/48/000000/greek-salad.png',
      name: '健身餐',
    },
    {
      icon: 'https://img.icons8.com/color/48/000000/fondue.png',
      name: '海底捞',
    },
    {
      icon: 'https://img.icons8.com/color/48/000000/noodles.png',
      name: '辛拉面',
    },
    {
      icon: 'https://img.icons8.com/color/48/000000/white-sesame-seeds.png',
      name: '炒饭',
    },
    {
      icon: 'https://img.icons8.com/color/48/000000/steak-medium.png',
      name: '牛排',
    },
  ];

  let showFoods = foods;
  let chance = 1;

  //整体打乱
  // function randomNumber() {
  //     return 0.5 - Math.random();
  // }
  // function randomFood() {
  //     foods.sort(randomNumber);
  //     foods.sort(randomNumber);
  //     foods.sort(randomNumber);
  //     foods = [...foods];
  // }

  function randomNumber() {
    return Math.floor(Math.random() * 9);
  }

  function randomFood() {
    let newFoods = [];
    let fingerIcon =
      'https://img.icons8.com/color/48/000000/one-finger--v1.png';
    let pickedNum = randomNumber();
    const rotate = [135, 180, 225, 90, 0, 270, 45, 0, 315];
    for (let i = 0; i < 9; i++) {
      newFoods.push({
        icon: fingerIcon,
        name: '',
        rotate: rotate[i],
      });
    }
    newFoods[4] = foods[pickedNum];
    showFoods = newFoods;
    chance = chance - 1;
  }
</script>

<section class="cardContainer">
  <div class="nes-container is-rounded outer-nes">
    <!-- <h3 class="title"></h3> -->
    <FoodSquare {showFoods} {foods} />
    <Controler bind:foods bind:chance {randomFood} />
  </div>
</section>

<style>
  .cardContainer {
    /* margin-bottom: 30px; */
    margin: 30px 6px auto 6px;
  }
  .outer-nes {
    padding-bottom: 1px;
  }
</style>
