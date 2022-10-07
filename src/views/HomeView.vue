<script setup>
import HeroImage from "../components/HeroImage.vue";
import IconPegaSilver from "../components/icons/IconPegaSilver.vue";
import ServicesSection from "../components/ServicesSection.vue";
import IconDiscord from "../components/icons/IconDiscord.vue";
import FooterSection from "../components/FooterSection.vue";
</script>

<template>
  <HeroImage />
  <main
    class="flex flex-col items-center gap-6 px-6 mt-[10vh] mb-[30vh] lg:flex-row lg:justify-between container-box"
  >
    <div class="flex flex-col gap-6">
      <h1>Play to Earn NFT based guild community. Come and Join Winners.</h1>
      <div class="flex flex-col gap-2">
        <span class="text-xs text-neutral-700">Winners Circle Guild</span>
        <button data-style-type="solid" class="button">
          <IconDiscord />
          <span>Join Discord Server</span>
        </button>
      </div>
    </div>
    <div
      class="relative min-h-[200px] mt-[240px] lg:mt-0 w-full md:max-w-[550px] p-[1px] rounded-2xl bg-gradient-to-br from-[#833A11] via-[#091011] to-[#6F540C]"
    >
      <div class="relative inset-0 w-full h-full rounded-2xl bg-[#090705]">
        <div class="p-6">
          <span class="block max-w-[36ch] text-neutral-500">
            <strong
              class="text-transparent bg-gradient-to-r from-[#9e4614] to-[#a38c25] text-clip bg-clip-text"
              >Pegaxy (Pegasus Galaxy)</strong
            >
            is a racing game with futuristic mythological styling. Pega (the
            horses) are descendants of the mighty Pegasus. In this game, players
            will participate in PvP format races to win rewards in the platforms
            native utility token, VIS (Vigorus).
          </span>
        </div>
        <IconPegaSilver />
      </div>
    </div>
  </main>
  <ServicesSection />
  <div class="container-box">
    <hr class="h-1 stroke-[1px] opacity-10 mt-10" />
  </div>
  <FooterSection />
</template>
