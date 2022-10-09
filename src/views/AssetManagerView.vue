<script setup>
import TextInput from "../components/ui/TextInput.vue";
import FooterSection from "../components/FooterSection.vue";
import IconPegaLogin from "../components/icons/IconPegaLogin.vue";
</script>

<template>
  <main class="relative container-box">
    <div class="relative flex items-center min-h-[85vh] justify-evenly">
      <IconPegaLogin class="opacity-80" />
      <div class="login-form">
        <div class="__content">
          <form>
            <h2 class="whitespace-nowrap">Welcome back!</h2>
            <span class="text-neutral-500"
              >Manage your NFT assets right at your fingertips.</span
            >
            <div class="flex flex-col gap-3 my-6">
              <TextInput type="text" placeholder="Email" />
              <TextInput type="password" placeholder="Password" />
            </div>
            <button data-style-type="solid" class="w-full py-4 button">
              Login
            </button>
            <button
              disabled
              data-style-type="outline"
              class="w-full py-4 mt-3 button"
            >
              Request for Access
            </button>
          </form>
        </div>
      </div>
    </div>
  </main>
  <FooterSection />
</template>

<script setup></script>
<style>
.login-form {
  @apply rounded-2xl p-[2px] max-w-[580px];
  @apply bg-gradient-to-br from-[#833A11] via-[#0E181A] to-[#6F540C];
}
.__content {
  @apply rounded-2xl p-6 flex flex-col gap-3 min-w-[370px];
  @apply bg-gradient-to-br from-[#090705] via-[#050504] to-[#0F0D09];
}
</style>
