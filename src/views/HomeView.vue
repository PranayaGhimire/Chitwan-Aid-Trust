<script setup>
import ContactLocation from '@/components/ContactLocation.vue';
import GetInvolved from '@/components/GetInvolved.vue';
import HeroSection from '@/components/HeroSection.vue';
import ImpactStatistics from '@/components/ImpactStatistics.vue';
import MissionSection from '@/components/MissionSection.vue';
import NewsUpdates from '@/components/NewsUpdates.vue';
import OurPrograms from '@/components/OurPrograms.vue';
import PartnersSponsors from '@/components/PartnersSponsors.vue';
import SuccessStories from '@/components/SuccessStories.vue';


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
