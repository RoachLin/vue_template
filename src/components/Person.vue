<script setup lang="ts">
import { reactive } from "vue";

/* ------------------------------------------------------------------------------------------ */

type Car = {
  brand: string;
  price: number;
};

const benz: Car = reactive({
  brand: "奔驰",
  price: 100,
});

function changePrice(): void {
  benz.price += 10;
}

/* ------------------------------------------------------------------------------------------ */

type Game = {
  id: string;
  name: string;
};

const games: Array<Game> = reactive([
  { id: "111", name: "王者" },
  { id: "222", name: "原神" },
  { id: "333", name: "三国" },
]);

function changeFirstName(): void {
  if (games[0]) {
    games[0].name = "魔兽世界";
  }
}
</script>

<template>
  <div class="person">
    <h2>汽车信息：一辆{{ benz.brand }}车，价值{{ benz.price }}万</h2>
    <button @click="changePrice">修改汽车的价格</button>
    <br />
    <h2>游戏列表：</h2>
    <ul>
      <li v-for="game in games">{{ game.name }}</li>
    </ul>
    <button @click="changeFirstName">修改第一个名字</button>
  </div>
</template>

<style scoped>
.person {
  background-color: skyblue;
}
</style>
