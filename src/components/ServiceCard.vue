<template>
  <div
    class="max-w-[697px] overflow-hidden min-h-[495px] relative bg-[#0f0c09] rounded-2xl transition-all group border border-transparent hover:border-neutral-600/50 hover:shadow-2xl"
  >
    <div
      class="relative w-full h-[300px] bg-gradient-to-t group-hover:bg-transparent from-black/50 to-amber-200/20"
    >
      <img
        :src="$props.image"
        alt="pegaxy"
        class="absolute inset-0 object-cover object-center w-full h-full transition-all mix-blend-soft-light group-hover:mix-blend-normal"
      />
    </div>
    <div class="relative flex flex-col gap-6 p-6 text-neutral-400">
      <div>
        <h2>{{ $props.title }}</h2>
        <span class="max-w-[60ch] block opacity-50 min-h-[48px]">{{
          $props.description
        }}</span>
      </div>
      <button
        :disabled="$props.disabled"
        @click="onClick"
        data-style-type="outline"
        class="button"
      >
        {{ $props.buttonLabel }}

        <IconArrowRight v-if="!$props.disabled" />
      </button>
    </div>
  </div>
</template>
<script setup>
import IconArrowRight from "./icons/IconArrowRight.vue";
defineProps({
  title: String,
  description: String,
  buttonLabel: String,
  image: String,
  disabled: Boolean,
});

function onClick() {
  console.log("clicked");
}
</script>
