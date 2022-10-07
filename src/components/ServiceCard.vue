<template>
  <div
    class="max-w-[697px] overflow-hidden min-h-[495px] relative bg-[#1a1613] rounded-2xl scale-95 hover:scale-100 transition-all"
  >
    <div
      class="relative w-full h-[300px] bg-gradient-to-t hover:bg-transparent from-black/50 to-amber-200/20"
    >
      <img
        :src="$props.image.toString()"
        alt="pegaxy"
        class="absolute inset-0 object-cover object-center w-full h-full transition-all mix-blend-soft-light hover:mix-blend-normal"
      />
    </div>
    <div class="relative flex flex-col gap-6 p-6 text-neutral-400">
      <div>
        <h2>{{ $props.title }}</h2>
        <span class="max-w-[60ch] block opacity-50 min-h-[48px]">{{
          $props.description
        }}</span>
      </div>
      <button @click="onClick" data-style-type="outline" class="button">
        {{ $props.buttonLabel }}

        <IconArrowRight />
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
});

function onClick() {
  console.log("clicked");
}
</script>
