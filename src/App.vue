<script setup>
import { ref } from "vue";
import { RouterLink, RouterView } from "vue-router";
import IconDiscord from "./components/icons/IconDiscord.vue";
import IconMenu from "./components/icons/IconMenu.vue";
import IconX from "./components/icons/IconX.vue";

const toggleMenu = ref(false);

function handleToggle() {
  toggleMenu.value = !toggleMenu.value;
}
</script>

<template>
  <header>
    <div class="container-box">
      <div class="wrapper">
        <RouterLink data-style-type="ghost" to="/">
          <div class="inline-flex items-center gap-1">
            <img
              class="w-10 h-10"
              src="@/assets/logo.svg"
              alt="winners circle logo"
            />
            <span class="hidden md:block">Winners' Circle Guild</span>
          </div>
        </RouterLink>
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
          <button
            @click="handleToggle"
            class="relative inline-flex items-center justify-center w-12 rounded-lg md:hidden bg-amber-100/5"
          >
            <Transition>
              <IconX
                class="absolute mx-auto stroke-amber-400"
                v-if="toggleMenu"
              />
              <IconMenu class="absolute mx-auto stroke-amber-400" v-else />
            </Transition>
          </button>
        </div>
      </div>
      <Transition>
        <div v-if="toggleMenu" class="block sm:hidden">
          <div class="flex flex-col gap-3 mt-6 nav-mobile">
            <RouterLink to="/">Home</RouterLink>
            <RouterLink to="/asset-manager">Asset Manager</RouterLink>
            <RouterLink to="/about">About</RouterLink>
          </div>
        </div>
      </Transition>
    </div>
  </header>

  <Suspense>
    <RouterView />
    <template #fallback>
      <div class="grid min-h-screen place-content-center">Loading...</div>
    </template>
  </Suspense>
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

.nav-mobile a {
  @apply dark:text-neutral-300 text-neutral-600 px-3 py-4;
}
</style>
