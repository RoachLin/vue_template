<script setup lang="ts">
import { ref } from "vue";

const firstName = ref<string>("");
const lastName = ref<string>("");
</script>

<template>
  <div class="person">
    姓：<input type="text" v-model="firstName" />
    <br />
    名： <input type="text" v-model="lastName" />
    <br />
    全名： <span>{{ firstName }}-{{ lastName }}</span>
    <br />
  </div>
</template>

<style scoped>
.person {
  background-color: skyblue;
}
</style>
