<template>
 <v-app class="background">
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
        return {};
    },
    components: { Header, Footer }
}
</script>
<style scoped>
    .v-application {
   font-family: Segoe UI , sans-serif !important; height: 100vh;
    
 }
 .background{
    background-image: url("../static/sections/masked1.png");
    background-repeat: no-repeat;
    background-size: 100% 100%;
    background-position: center;
    background-origin: content-box;
    top: -2px;
}
</style>
