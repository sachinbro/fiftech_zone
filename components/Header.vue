<script>
export default{
    created () {
    window.addEventListener('scroll', this.onScroll);
    
  },
    data(){
        return {
            scroll: 0,
            drawer: false,
            links: [
                {
                    name: 'About Us',
                    url: '/about'
                },
                    {
                        name: 'Services',
                        url: '/services'
                    },
                {
                    name: 'Projects',
                    url: '/projects'
                },
                {
                    name: 'Testimonials',
                    url: '/testimonials'
                },
                {
                    name: 'Career',
                    url: '/career'
                },
                {
                    name: 'Contact Us',
                    url: '/contact'
                }
            ]
        }

    },
    methods: {
        onScroll(e){
            this.scroll = e.target.documentElement.scrollTop
            // console.log("scroll", e.target.documentElement.scrollTop);
        },
        
    },
    computed:{
        makeSticky(){
            return this.scroll > 50;
        }
    }
}
</script>
<template>
<div >
    <v-app-bar  elevation="4"  height="50"   color="navBackground" >
        <div class="d-flex align-start mb-3" >
            <img src="../static/icons/fb.svg" width="25" height="25" alt="">
            <img src="../static/icons/twitter.svg" width="25" height="25" alt="">
            <img src="../static/icons/insta.svg" width="25" height="25" alt="">
        </div>
        
        <v-spacer></v-spacer>
        <v-spacer></v-spacer>
        <v-row class="d-flex justify-space-around mb-4 ">
            <div>
                <v-icon color="white">mdi-phone</v-icon>
                <span class="white--text text-caption hidden-sm-and-down">9846907090</span>
            </div>
            <div>
                <v-icon color="white">mdi-email-outline</v-icon>
                <span class="white--text text-caption hidden-sm-and-down">fiftechzone@gmail.com</span>
            </div>
            <div>
                <v-icon dark>mdi-clock-outline</v-icon>
                <span class="white--text text-caption hidden-sm-and-down">10 A.M to 5 P.M</span>
            </div>
        </v-row>
    </v-app-bar>
    <v-app-bar 
    class="sticky "
    :app="makeSticky"
    height="70"
    dark
    color="navBackground"
    
    >   <div class="pl-16">
        <nuxt-link to="/">
            <img class="" src="../static/icons/fiftechlogo.svg" height="70px">
        </nuxt-link>
        </div>
            
        <v-spacer></v-spacer>
        <v-spacer></v-spacer>
        <v-row class="d-none d-sm-flex justify-space-around white--text " no-gutters>
            <nuxt-link to="/about" class="white--text link">About Us</nuxt-link>
            <nuxt-link to="/services" class="white--text link">Services</nuxt-link>
            <nuxt-link to="projects" class="white--text link">Projects</nuxt-link>
            <nuxt-link to="/testimonials" class="white--text link">Testimonials</nuxt-link>
            <nuxt-link to="/career" class="white--text link">Career</nuxt-link>
            <nuxt-link to="/contact" class="white--text link">Contacts</nuxt-link>
        </v-row>
        <v-row class="d-flex d-sm-none navigation-drawer justify-end align-middle">
            <v-app-bar-nav-icon  @click.stop="drawer= !drawer" ></v-app-bar-nav-icon>
            <v-navigation-drawer
            v-model="drawer"
            class=" black--text  navigation-drawer"
           
            height="400"
            width="400"
            app
            right
            temporary
            >
            <v-card dark>
                <div class="navBackground white--text d-flex align-center text-h5"> <nuxt-link to="/"><img src="../static/icons/fiftechlogo.svg" alt=""></nuxt-link> <span class="ml-n4"> iftechZone</span> </div>
            <v-list>
                <v-list-item-group>
                    <v-list-item v-for="link in links" :key="link.url" style="border: 1px #DCD4D4 solid;">
                    <v-list-icon>
                        <v-icon light>mdi-view-dashboard</v-icon>
                    </v-list-icon>
                    <v-list-item-content>
                        <v-list-item-title >
                           <nuxt-link :to="link.url" class="link black--text">
                               {{link.name}}
                           </nuxt-link> 
                            </v-list-item-title>
                    </v-list-item-content>
                </v-list-item> 
                </v-list-item-group>
                
            </v-list>
            </v-card>
            
            </v-navigation-drawer>
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
    .v-navigation-drawer, .v-overlay__scrim {
        z-index: 999999 !important;
        }
</style>