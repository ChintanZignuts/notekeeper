<script setup>
import { ref, computed } from "vue";
import { useRoute } from "vue-router";

const route = useRoute();

const menuItems = [
  { title: "Sign Up", path: "/signup", icon: "face" },
  { title: "Sign In", path: "/signin", icon: "lock_open" },
];
console.log(route.path);
const isSignUpOrSignInRoute = computed(() => {
  return route.path === "/signup" || route.path === "/signin";
});
</script>
<template>
  <VToolbar dark prominent>
    <v-toolbar-title>NoteKeeper</v-toolbar-title>

    <v-spacer></v-spacer>

    <NuxtLink v-if="isSignUpOrSignInRoute" to="/">Home</NuxtLink>

    <NuxtLink
      v-if="!isSignUpOrSignInRoute"
      v-for="menuItem in menuItems"
      :key="menuItem.path"
      :to="menuItem.path"
    >
      <v-btn class="text-none">{{ menuItem.title }}</v-btn>
    </NuxtLink>
  </VToolbar>
</template>
