<template>
  <div>
    <Intro />
    <OfferSection />
  </div>
</template>

<script>
import Intro from '../components/sections/home-page-sections/HomePageIntro.vue';
import OfferSection from '../components/sections/home-page-sections/OfferSection.vue';
export default {
    name: "IndexPage",
    components: { Intro, OfferSection }
}
</script>
