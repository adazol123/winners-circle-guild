<template>
  <section class="container-box">
    <div class="about">
      <IconWInnersCircle />
      <h1>Winners Circle Guild</h1>
      <div class="flex flex-col items-center gap-6 py-6 my-10 text-neutral-500">
        <p class="text-center max-w-[80ch]">
          Winners Circle Guild is Play To Earn Community on Discord Server,
          Stablished Year 2021. Providing Potential earning by playing WEB3
          based online games (NFT). Granted Scholars will received a portion of
          their total earning from play games, currently the game winners' cicle
          guild offers is Pegaxy NFT Games.
        </p>
        <div class="relative min-h-[690px]">
          <img
            src="@/assets/thumbnail-discord-server.png"
            alt="discord server"
          />
        </div>
      </div>
    </div>
  </section>
  <div class="container-box">
    <hr class="h-1 stroke-[1px] opacity-10 mt-10" />
  </div>
  <FooterSection />
</template>

<script setup>
import IconWInnersCircle from "../components/icons/IconWInnersCircle.vue";
import FooterSection from "../components/FooterSection.vue";
</script>

<style>
.about {
  @apply flex flex-col items-center;
}
</style>
