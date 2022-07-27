<script>
import AboutIntro from '../components/sections/about-page/AboutIntro.vue';
import VisionMission from '../components/sections/about-page/VisionMission.vue';

export default {
    name: "AboutPage",
    components: { AboutIntro, VisionMission }
}
</script>
<template>
    <div>
       <AboutIntro />
       <VisionMission />
    </div>
</template>
