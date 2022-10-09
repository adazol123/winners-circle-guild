<template>
  <section class="mt-[10vh] container-box">
    <div
      class="flex flex-wrap items-center justify-center gap-10 mx-auto w-fit"
    >
      <ServiceCard
        description="Earn while you are playing your favorite game at the same time with
          Pegaxy."
        title="Pegaxy Game Scholarship"
        button-label="Explore Game"
        :image="asset1"
      />
      <ServiceCard
        description="Manage and Track your valuable NFT assets in one place. Renting assets to scholars, Identify high earner NFT assets."
        title="Winners Circle Asset Managerment"
        button-label="Early Access"
        :image="asset2"
      />
      <ServiceCard
        description="Automate the way you check the stats on your assets. Scholars can check their rented assets."
        title="Winners Circle Discord BOT"
        button-label="Get Discord BOT"
        :image="asset3"
      />
      <ServiceCard
        description="Answer all your queries and concern with your discord server.Resolve incidents on real time chat environment."
        title="Helpdesk BOT"
        button-label="Coming Soon"
        :image="asset4"
        disabled
      />
    </div>
  </section>
</template>

<script setup>
import ServiceCard from "./ServiceCard.vue";
import asset1 from "../assets/thumbnail-pegaxy.png";
import asset2 from "../assets/thumbnail-winners-circle.png";
import asset3 from "../assets/thumbnail-winners-circle-bot.png";
import asset4 from "../assets/thumbnail-helpdesk-bot.png";
</script>

<style scoped></style>
