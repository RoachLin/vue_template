<script setup lang="ts">
import { ref } from "vue";

const name = ref<string>("张三");
const age = ref<number>(18);
const tel: string = "13811112222";
const address: string = "广州市";

function changeName(): void {
  name.value = "zhang_san";
}

function changeAge(): void {
  age.value++;
}

function showTel(): void {
  alert(tel);
}
</script>

<template>
  <div class="person">
    <h2>姓名：{{ name }}</h2>
    <h2>年龄：{{ age }}</h2>
    <h2>地址：{{ address }}</h2>
    <hr />
    <button @click="changeName">修改名字</button>
    <button @click="changeAge">修改年龄</button>
    <button @click="showTel">查看联系方式</button>
  </div>
</template>

<style scoped>
.person {
  background-color: skyblue;
}
</style>
