<script>

</script>
<template>
<div >
    <v-app-bar elevation="4"  height="50" elevate-on-scroll color="navBackground">
        <div class="d-flex align-start mb-3">
            <img src="../static/icons/fb.svg" width="25" height="25" alt="">
            <img src="../static/icons/twitter.svg" width="25" height="25" alt="">
            <img src="../static/icons/insta.svg" width="25" height="25" alt="">
        </div>
        
        <v-spacer></v-spacer>
        <v-spacer></v-spacer>
        <v-row class="d-flex justify-space-around mb-4 ">
            <div>
                <v-icon color="white">mdi-phone</v-icon>
                <span class="white--text text-caption">9846907090</span>
            </div>
            <div>
                <v-icon color="white">mdi-email-outline</v-icon>
                <span class="white--text text-caption">fiftechzone@gmail.com</span>
            </div>
            <div>
                <v-icon dark>mdi-clock-outline</v-icon>
                <span class="white--text text-caption">10 A.M to 5 P.M</span>
            </div>
        </v-row>
    </v-app-bar>
    <v-app-bar 
    class="sticky"
    height="70"
    color="navBackground"
    
    >   <div class="pl-16">
        <nuxt-link to="/">
            <img class="" src="../static/icons/fiftechlogo.svg" height="70px">
        </nuxt-link>
        </div>
            
        <v-spacer></v-spacer>
        <v-spacer></v-spacer>
        <v-row class="d-flex justify-space-around white--text" no-gutters>
            <nuxt-link to="/about" class="white--text link">About Us</nuxt-link>
            <nuxt-link to="#" class="white--text link">Services</nuxt-link>
            <nuxt-link to="#" class="white--text link">Projects</nuxt-link>
            <nuxt-link to="#" class="white--text link">Testimonials</nuxt-link>
            <nuxt-link to="#" class="white--text link">Career</nuxt-link>
            <nuxt-link to="#" class="white--text link">Contacts</nuxt-link>
        </v-row>
        
    </v-app-bar>
</div>
    
</template>
<style scoped>
    .navBackground {
       background: transparent linear-gradient(10deg, #9B51E0 0%, #347FE2 76%, #0693E3 100%) 0% 0% no-repeat padding-box;
           }
    .link{
       font: normal normal bold 15px Segoe UI;
        text-decoration: none;
        border-radius: 20px;
        padding: 2px;
    }
     .link:hover{
        background-color: white;
        color: #9B51E0 !important;
    }
    .sticky{
 
    }
</style>