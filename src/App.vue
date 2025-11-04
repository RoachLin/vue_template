<script setup lang="ts">
import { RouterLink, RouterView } from "vue-router";
import Person from "./components/Person.vue";
</script>

<template>
  <Person />

  <nav>
    <RouterLink to="/">Home</RouterLink>
    <RouterLink to="/about">About</RouterLink>
  </nav>
  <RouterView />
</template>

<style scoped></style>
