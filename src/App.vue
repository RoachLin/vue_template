<script setup lang="ts">
import { RouterLink, RouterView } from "vue-router";
import Person from "./components/Person.vue";
</script>

<template>
  <nav>
    <RouterLink to="/">Home</RouterLink>
    <RouterLink to="/about">About</RouterLink>
  </nav>

  <RouterView />

  <Person />
</template>

<style scoped></style>
