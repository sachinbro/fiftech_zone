<script>
import ServicesIntroVue from "../components/sections/services-page/ServicesIntro.vue";
import ServicesIntro from "../components/sections/services-page/ServicesIntro.vue";
import Carousel3D from "../components/sections/services-page/Carousel3D.vue";
import ServicePlan from "../components/sections/services-page/ServicePlan.vue";
    export default{
    components: { ServicesIntro, Carousel3D, ServicePlan }
}
</script>
<template>
    <div>
        <ServicesIntro />
        <Carousel3D />
        <ServicePlan />
    </div>
</template>