<template>
 <v-app :class="background">
  <Header />
  <v-main>
      <Nuxt />
  </v-main>
  <Footer />
 </v-app>
</template>

<script>
import Header from '../components/Header.vue'
import Footer from '../components/Footer.vue';
export default {
    name: "DefaultLayout",
    data() {
        return {
            background: "homebackground"
        };
    },
    components: { Header, Footer },
     watch:{
            '$route'(to,from){
                console.log(to.path)
                if(to.path == "/"){
                    this.background = "homebackground"
                    return
                }
                this.background = "otherNavBackground"
            }
        }
}
</script>
<style scoped>
    .v-application {
   font-family: Segoe UI , sans-serif !important; height: 100vh;
    
 }
 .homebackground{
    background-image: url("../static/sections/masked.png");
    background-repeat: no-repeat;
    background-size: 100% 100%;
    background-position: center;
    background-origin: content-box;
    top: -2px;
}
.otherNavBackground{
   background-image: url("../static/sections/Servicespage/background.png");
    background-repeat: no-repeat;
    background-size: 100% 70%;
    background-position: top;
    background-origin: content-box;
    top: -2px;
}
</style>
