<template>
  <div>
    <Intro />
    <OfferSection />
    <WorkExperience />
    <ProjectInfo />
    <HomeTestimonials />
  </div>
</template>

<script>
import Intro from '../components/sections/home-page-sections/HomePageIntro.vue';
import OfferSection from '../components/sections/home-page-sections/OfferSection.vue';
import WorkExperience from '../components/sections/home-page-sections/WorkExperience.vue';
import ProjectInfo from '../components/sections/home-page-sections/ProjectInfo.vue';
import HomeTestimonials from '../components/sections/home-page-sections/HomeTestimonials.vue';
export default {
    name: "IndexPage",
    components: { Intro, OfferSection, WorkExperience, ProjectInfo, HomeTestimonials },
    data(){
      return{
          target: "#testimonials",
      }
    }, computed:{

        options () {
        return {
          duration: 500,
          offset: 0,
          easing: "easeInOutCubic",
        }
      },
    },
    watch:{
        '$route'(to, from){
            console.log("to", from);
            if(to.hash === "#testimonials"){
                this.$vuetify.goTo(this.target, this.options)
            }
            if(to.hash === "#footer"){
              this.$vuetify.goTo("#footer", this.options)
            }
        }
    }
}
</script>
