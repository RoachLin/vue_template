<script setup lang="ts">
import { computed, ref } from "vue";

const firstName = ref<string>("");
const lastName = ref<string>("");

const fullName = computed<string>(() => {
  return firstName.value.slice(0, 1).toUpperCase() + firstName.value.slice(1) + "-" + lastName.value;
});
</script>

<template>
  <div class="person">
    姓：<input type="text" v-model="firstName" />
    <br />
    名： <input type="text" v-model="lastName" />
    <br />
    全名： <span>{{ fullName }}</span>
    <br />
  </div>
</template>

<style scoped>
.person {
  background-color: skyblue;
}
</style>
