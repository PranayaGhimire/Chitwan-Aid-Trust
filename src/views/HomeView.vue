<script setup>
import ContactLocation from '@/components/Home/ContactLocation.vue';
import GetInvolved from '@/components/Home/GetInvolved.vue';
import HeroSection from '@/components/Home/HeroSection.vue';
import ImpactStatistics from '@/components/Home/ImpactStatistics.vue';
import MissionSection from '@/components/Home/MissionSection.vue';
import NewsUpdates from '@/components/Home/NewsUpdates.vue';
import OurPrograms from '@/components/Home/OurPrograms.vue';
import PartnersSponsors from '@/components/Home/PartnersSponsors.vue';
import SuccessStories from '@/components/Home/SuccessStories.vue';
</script>

<template>
  <main>
      <HeroSection/>
      <MissionSection/>
      <ImpactStatistics/>
      <OurPrograms/>
      <SuccessStories/>
      <GetInvolved/>
      <NewsUpdates/>
      <PartnersSponsors/>
      <ContactLocation/>
  </main>
</template>
