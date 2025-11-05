<script setup lang="ts">
import { reactive, toRefs, toRef, type Ref } from "vue";

/* ------------------------------------------------------------------------------------------ */

type Person = {
  name: string;
  age: number;
};

const person: Person = reactive({
  name: "张三",
  age: 18,
});

const { name: name1, age: age1 } = toRefs(person);

function changeName(): void {
  name1.value += "~";
}

function changeAge(): void {
  age1.value += 1;
}

/* ------------------------------------------------------------------------------------------ */

const age2: Ref<number> = toRef(person, "age");
</script>

<template>
  <div class="person">
    <h2>姓名：{{ name1 }}</h2>
    <h2>年龄：{{ age1 }}，{{ age2 }}</h2>
    <button @click="changeName">修改名字</button>
    <button @click="changeAge">修改年龄</button>
  </div>
</template>

<style scoped>
.person {
  background-color: skyblue;
}
</style>
