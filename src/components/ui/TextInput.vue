<template>
  <input :type="$props.type" :placeholder="$props.placeholder" />
</template>

<script setup>
defineProps({
  type: String,
  placeholder: String,
});
</script>

<style scoped>
input {
  @apply text-neutral-300 placeholder:opacity-50;
}
</style>
