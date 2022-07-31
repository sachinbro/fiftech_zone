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
    components: { PriceBtn }
}
</script>
<template>
    <div class="mt-12">
        <div>
            <v-row class="my-16">
                <v-col cols="4"></v-col>
                <v-col class="text-center" cols="3">
                    <v-row>
                        <v-col class="text-center">
                            <p class="text-left"><span class="text-h5 " style="border-bottom: 3px solid #707070">Basic Plan</span></p>
                            <ul class="text-left">
                                <li v-for="plan in plans.basic" :key="plan" class="my-1">{{plan}}</li>
                            </ul>
                           <PriceBtn price="20,000"/>
                        </v-col>
                        
                    </v-row>
                </v-col>
                <v-col>
                    <img src="../../../static/sections/Servicespage/Image 43.png" height="240px" alt="">
                </v-col>
                <v-col cols="1"></v-col>
            </v-row>
            <v-row>
                <v-col cols="4"></v-col>
                <v-col cols="3">
                    <img src="../../../static/sections/Servicespage/Image 41.png" height="240px" alt="">
                </v-col>
                <v-col class="text-center">
                    <v-row>
                        <v-col class="text-left">
                            <p class="text-left"><span class="text-h5 " style="border-bottom: 3px solid #707070">Standard Plan</span></p>
                            <ul class="text-left">
                                <li v-for="plan in plans.standard" :key="plan" class="my-1">{{plan}}</li>
                            </ul>
                            <div class="mx-10"><PriceBtn price="60,000"/></div>
                            
                        </v-col>
                        <v-col cols="1"></v-col>
                    </v-row>
                </v-col>
            </v-row>
            <v-row class="my-16">
                <v-col cols="4"></v-col>
                <v-col class="text-center" cols="3">
                    <v-row>
                        <v-col>
                            <p class="text-left"><span class="text-h5 " style="border-bottom: 3px solid #707070">Premium Plan</span></p>
                            <ul class="text-left">
                                <li v-for="plan in plans.premium" :key="plan" class="my-1">{{plan}}</li>
                            </ul>
                            <PriceBtn price="100,000"/>
                        </v-col>
                        
                    </v-row>
                </v-col>
                <v-col>
                    <img src="../../../static/sections/Servicespage/Image 42.png" height="240px" alt="">
                </v-col>
                <v-col cols="1"></v-col>
            </v-row>
            <v-row class="mb-16">
                <v-col cols="4"></v-col>
                <v-col cols="3">
                    <img src="../../../static/sections/Servicespage/Image 44.png" height="240px" alt="">
                </v-col>
                <v-col class="text-center">
                    <v-row>
                        <v-col class="text-left">
                            <p class="text-left"><span class="text-h5 " style="border-bottom: 3px solid #707070">Corporate Plan</span></p>
                            <ul class="text-left">
                                <li v-for="plan in plans.corporate" :key="plan" class="my-1">{{plan}}</li>
                            </ul>
                            <div class="mx-10">
                                <PriceBtn/>
                            </div>
                        </v-col>
                        <v-col cols="1"></v-col>
                    </v-row>
                </v-col>
            </v-row>
        </div>
    </div>
</template>