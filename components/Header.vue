<script>
export default{
    created () {
    window.addEventListener('scroll', this.onScroll);
  },
  mounted(){
     

  },
  
    data(){
        return {
            scroll: 0,
            target: "#testimonials",
            background: "navBackground",
            drawer: false,
            socialIcons: [
                "facebook", "twitter", "instagram",
            ],

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
                    name: 'Testimonials',
                    url: '/#testimonials'
                },
                {
                    name: 'Career',
                    url: '/career'
                },
                {
                    name: 'Contact Us',
                    url: '/#footer'
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
        },
        
    },
        watch:{
            '$route'(to,from){
                if(to.path == "/"){
                    this.background = "navBackground"
                    return
                }
                this.background = "otherNvaBackground"
            }
        }
    

}
</script>
<template>
<div >
    <v-app-bar flat elevation="0"  height="50"   :class="makeSticky ? background : ''" color="transparent">
        <div class="d-flex align-start mb-3 ">
            <v-icon v-for="icon in socialIcons" :key="icon" class="mx-1" size="large" dark>mdi-{{icon}}</v-icon>
            
        </div>
        <v-spacer></v-spacer>
        <v-spacer></v-spacer>
        <v-spacer></v-spacer>
        <v-row class="d-flex justify-space-around mb-4 mt-0 mt-sm-2 ">
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
        <v-spacer class="d-none d-sm-flex"></v-spacer>
    </v-app-bar>
    <v-app-bar 
    color="transparent"
    class="stick "
    :class="makeSticky ? background : ''"
    :app="makeSticky"
    elevation="0"
    height="70"
    >   <div class="pl-16">
        <a href="/">
            <img class="" src="../static/icons/fiftechlogo.svg" height="70px">
        </a>
        </div>
            
        <v-spacer></v-spacer>
        <v-spacer></v-spacer>
        <v-spacer></v-spacer>
        <v-row class="d-none d-sm-flex justify-space-around white--text" no-gutters>
            <nuxt-link v-for="link in links" :key="link.title" :to="`${link.url}`" class="white--text link px-3 py-1">{{link.name}}</nuxt-link>
            
        </v-row>
        <v-spacer class="d-none d-sm-flex"></v-spacer>
        <v-row class="d-flex d-sm-none justify-end ">
            <v-app-bar-nav-icon  @click.stop="drawer= !drawer" dark ></v-app-bar-nav-icon>
           
        </v-row>
        
    </v-app-bar>
     <v-navigation-drawer class="mt-15"
            v-model="drawer"
            height="500"
            width="250"
            app
            right
            temporary
            
            >
                    <div class="navBackground white--text d-flex align-center font-weight-bold">
                        <a href="/"><img src="../static/icons/fiftechlogo.svg" height="50" class="ml-2"></a><span class="ml-n4">iftechzone</span> </div>
                    <v-list
                    nav
                    dense
                >
                    <v-list-item-group
                    
                    active-class="deep-purple--text text--accent-4"
                    >
                    <v-list-item v-for="link in links" :key="link.title" style="border-bottom: 2px solid #DCD4D4; border-radius:0%;">
                        <v-list-item-title><nuxt-link  :to="`${link.url}`" class="link">{{link.name}} <br> </nuxt-link> </v-list-item-title>
                    </v-list-item>

                    </v-list-item-group>
                </v-list>
            
            </v-navigation-drawer>
</div>
    
</template>
<style scoped>
    .navBackground {
       background: transparent linear-gradient(100deg,  #0693E3 0%, #347FE2 36%, #9B51E0 100%) 0% 0% no-repeat padding-box;
    }
    .otherNvaBackground{
        background: transparent linear-gradient(100deg, #9B51E0 100%, #347FE2 76%, #0693E3 30%) 0% 0% no-repeat padding-box;    }
    .link{
       font: normal normal bold 15px Segoe UI;
        text-decoration: none;
        border-radius: 20px;
        padding: 3px;
    }
     .link:hover{
        background-color: white;
        color: #9B51E0 !important;
    }
    /* .v-navigation-drawer, .v-overlay__scrim {
        z-index: 999999 !important;
        } */
    .nuxt-link-exact-active{

        background-color: white;
        color: #9B51E0 !important;
    }
</style>