<script setup>
import IconPegaSilver from "../components/icons/IconPegaSilver.vue";
import TextInput from "../components/ui/TextInput.vue";
</script>

<template>
  <main class="relative container-box">
    <div class="relative flex">
      <IconPegaSilver />
      <div class="login-form">
        <div class="__content">
          <h1>Welcome back!</h1>
          <span>Manage your NFT assets right at your fingertips.</span>
          <div class="flex flex-col gap-3 my-6">
            <TextInput />
            <TextInput />
          </div>
          <button data-style-type="solid" class="w-full py-4 button">
            Login
          </button>
          <button data-style-type="ghost" class="w-full py-4 button">
            Register
          </button>
        </div>
      </div>
    </div>
  </main>
</template>

<style>
.login-form {
  @apply rounded-2xl p-[1px] max-w-[580px];
  @apply bg-gradient-to-br from-[#833A11] via-[#0E181A] to-[#6F540C];
}
.__content {
  @apply rounded-2xl p-6 flex flex-col gap-3;
  @apply bg-gradient-to-br from-[#090705] via-[#050504] to-[#0F0D09];
}
</style>
