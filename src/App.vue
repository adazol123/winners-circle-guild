<script setup>
import { RouterLink, RouterView } from "vue-router";
import IconDiscord from "./components/icons/IconDiscord.vue";
</script>

<template>
  <header>
    <div class="container-box">
      <div class="wrapper">
        <div class="inline-flex items-center gap-1">
          <img
            class="w-10 h-10"
            src="@/assets/logo.svg"
            alt="winners circle logo"
          />
          <span class="hidden md:block">Winners' Circle Guild</span>
        </div>
        <div class="nav-menu">
          <nav>
            <RouterLink to="/">Home</RouterLink>
            <RouterLink to="/asset-manager">Asset Manager</RouterLink>
            <RouterLink to="/about">About</RouterLink>
          </nav>
          <button data-style-type="solid" class="button">
            <IconDiscord />
            Discord
          </button>
        </div>
      </div>
    </div>
  </header>

  <RouterView />
</template>

<style scoped>
header {
  line-height: 1.5;
  max-height: 100vh;
  position: sticky;
  top: 0;
  left: 0;
  right: 0;
  z-index: 40;
  /* margin: 24px, 0; */
  /* box-shadow: 0px 1px 16px rgba(51, 51, 51, 0.11); */
  @apply py-3 backdrop-blur-sm bg-black/30;
  /* @apply bg-white dark:bg-gradient-to-r dark:from-gray-900 dark:to-black; */
}
.wrapper {
  @apply dark:text-neutral-300 text-neutral-600 flex w-full items-center justify-between min-h-[var(--nav-height)];
}
nav {
  @apply gap-3 items-center hidden sm:flex;
}

nav a {
  @apply dark:text-neutral-300 text-neutral-600 px-3 py-4;
}
.nav-menu {
  @apply flex gap-3;
}
</style>
