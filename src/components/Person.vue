<script setup lang="ts">
import { ref, reactive } from "vue";

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

const sum = ref<number>(0);

function changeSum(): void {
  sum.value += 1;
}
</script>

<template>
  <div class="person">
    <h2>汽车信息：一辆{{ benz.brand }}车，价值{{ benz.price }}万</h2>
    <button @click="changePrice">修改汽车的价格</button>
    <hr />
    <h2>当前求和为：{{ sum }}</h2>
    <button @click="changeSum">点我sum+1</button>
  </div>
</template>

<style scoped>
.person {
  background-color: skyblue;
}
</style>
