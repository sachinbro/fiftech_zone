<script>
import PriceBtn from "../../reusables/PriceBtn.vue";
export default {
    data() {
        return {
            plans: {
                basic: [
                    "5 static pages",
                    "Social Media Integration",
                    "1 Design Concept",
                    "1 Revision Session",
                    "Homepage SEO",
                    "Domain",
                    "Basic Hosting"
                ],
                standard: [
                    "15 pages",
                    "Basic CMS",
                    "News Letter Form",
                    "Contract Form",
                    "2 Design Concept",
                    "3 Revision Session",
                    "SEO Friendly",
                    "Standard Hosting",
                ],
                premium: [
                    "25 pages",
                    "Advanced CMS",
                    "Email integration",
                    "5 Revision session",
                    "3 Design Concept",
                    "SEO Friendly",
                    "Advance search engine"
                ],
                corporate: [
                    "Unlimited static and dynamic pages",
                    "Customizable Content Management System",
                    "Database integration",
                    "e-commerce functionality",
                    "Chat, social medai, Email integration",
                    "Unlimited Design Concepts",
                    "Unlimited Revision Sessions",
                    "Advanced hosting",
                    "Advanced search engine",
                    "Customizable features",
                    "Order management"
                ]
            }
        };
    },
    components: { PriceBtn },
    computed: {
      screen() {
        switch (this.$vuetify.breakpoint.name) {
          case 'xs':
            return '240px'
          case 'sm':
            return '50px'
          default :
            return '340px'
        }
      }
    }
}
</script>
<template>
<div class="mt-12">
        <div>
            <v-row class="my-16 left">
                <v-col cols="2" sm="3"></v-col>
                <v-col class="text-center" cols="8" sm="4">
                    <v-row class="flex-column">

                            <p class="text-left"><span class="text-h5 " style="border-bottom: 3px solid #707070">Basic Plan</span></p>
                            <ul class="text-left">
                                <li v-for="plan in plans.basic" :key="plan" class="my-1">{{plan}}</li>
                            </ul>
                            <div class="ml-2 ml-sm-10 mt-2 d-flex ">
                                <PriceBtn price="20,000"/>
                            </div>


                    </v-row>
                </v-col>
                <v-col cols="12"  sm="auto" class="d-flex justify-center mt-3 mt-sm-0">
                    <img src="../../../static/sections/Servicespage/Image 43.png" :height="screen" alt="">
                </v-col>
                <v-col cols="1"></v-col>
            </v-row>
            <v-row class="my-16 right">
                <v-col cols="0" sm="3"></v-col>
                <v-col cols="4" class="d-none d-sm-block">
                    <img src="../../../static/sections/Servicespage/Image 41.png" :height="screen" alt="">
                </v-col>
                <v-col class="text-center" cols="12" sm="4">
                    <v-row>
                       <v-col cols="2" md="0"></v-col>
                        <v-col class=" text-left  ml-sm-0" cols="auto" sm="11">
                            <p class=""><span class="text-h5 " style="border-bottom: 3px solid #707070">Standard Plan</span></p>
                            <ul class="">
                                <li v-for="plan in plans.standard" :key="plan" class="my-sm-1">{{plan}}</li>
                            </ul>
                            <div class="mt-2 mx-sm-10"><PriceBtn price="60,000"/></div>
                        </v-col>
                        <v-col cols="0" sm="1"></v-col>
                    </v-row>
                </v-col>

                <v-col cols="12" class="d-flex d-sm-none justify-center">
                    <img src="../../../static/sections/Servicespage/Image 41.png" :height="screen" alt="">
                </v-col>
            </v-row>
            <v-row class="my-16 left">
                <v-col cols="2" sm="3"></v-col>
                <v-col class="text-center" cols="6" sm="4">
                    <v-row class="flex-column">

                            <p class="text-left"><span class="text-h5 " style="border-bottom: 3px solid #707070">Premium Plan</span></p>
                            <ul class="text-left">
                                <li v-for="plan in plans.premium" :key="plan" class="my-1">{{plan}}</li>
                            </ul>
                            <div class="mx-sm-10 mt-2 d-flex ">
                                <PriceBtn price="1,00,000"/>
                            </div>


                    </v-row>
                </v-col>
                <v-col  cols="12"  sm="auto" class="d-flex justify-center">
                    <img src="../../../static/sections/Servicespage/Image 42.png" :height="screen" alt="">
                </v-col>
                <v-col cols="1"></v-col>
            </v-row>

             <v-row class="my-16 right">
                <v-col cols="3"></v-col>
                <v-col cols="4" class="d-none d-sm-block">
                    <img src="../../../static/sections/Servicespage/Image 44.png" :height="screen" alt="">
                </v-col>
                <v-col class="text-center" cols="12" sm="4">
                    <v-row>
                        <v-col cols="2" md="0"></v-col>
                        <v-col class="text-left  ml-sm-0" cols="9" sm="11">
                            <p class="text-left"><span class="text-h5 " style="border-bottom: 3px solid #707070">Corporate Plan</span></p>
                            <ul class="text-left">
                                <li v-for="plan in plans.corporate" :key="plan" class="my-1">{{plan}}</li>
                            </ul>
                            <div class="mx-10"><PriceBtn /></div>

                        </v-col>
                        <v-col cols="1"></v-col>
                    </v-row>
                </v-col>
                 <v-col cols="12" class="d-flex d-sm-none justify-center">
                    <img src="../../../static/sections/Servicespage/Image 44.png" :height="screen" alt="">
                </v-col>
            </v-row>
        </div>
    </div>
    
</template>
<style scoped>
/* .left{
       display: flex;
       align-content: center;
        height: 70vh;
        background-image: url("../../../static/sections/Servicespage/sideleft.png");
        background-repeat: no-repeat;
        background-size: 50% 100%;
        background-position: left;
        background-origin: content-box;
}
.right{
       display: flex;
       align-content: center;
        height: 70vh;
        background-image: url("../../../static/sections/Servicespage/side.png");
        background-repeat: no-repeat;
        background-size: 55% 100%;
        background-position: right;
        background-origin: content-box;
} */
</style>
