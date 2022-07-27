<script>
import AboutIntro from '../components/sections/about-page/AboutIntro.vue';
import VisionMission from '../components/sections/about-page/VisionMission.vue';
import PrimaryValues from '../components/sections/about-page/PrimaryValues.vue';

export default {
    name: "AboutPage",
    components: { AboutIntro, VisionMission, PrimaryValues }
}
</script>
<template>
    <div>
       <AboutIntro />
       <VisionMission />
       <PrimaryValues />
    </div>
</template>
