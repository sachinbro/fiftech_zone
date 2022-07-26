<template>
<div>
        <div class="purple">
            <div class="footer-main white--text">
                <v-row>
                    
                    <v-col class="">
                    <img src="../static/Footer/Group 318.png" alt="" class="px-16">
                        <p class="mt-n10 pl-3">Digitalize your business with our product services. Let the world know where you stand in the market.</p>
                    </v-col>
                    <v-col>
                        <p class="text-h5 font-weight-bold">Get In Touch</p>
                        <div class="mt-10">
                            <p><v-icon dark>mdi-map-marker</v-icon> Shantinagar, Kathmandu</p>
                            <p><v-icon dark>mdi-email-outline</v-icon> fiftechzone@gmail.com</p>
                            <p><v-icon dark>mdi-phone</v-icon> 981-15790629</p>
                        </div>
                    </v-col>
                    <v-col>
                        <p class="text-h5 font-weight-bold">Explore</p>
                        <div class="mt-10">
                            <p>About US</p>
                            <p>Service</p>
                            <p>Projects</p>
                            <p>Testimonials</p>
                        </div>
                    </v-col>
                    <v-col class="">
                        <p class="text-h5 font-weight-bold text-center">Follow us</p>
                        <div class="px-2  d-flex justify-center">
                            <v-icon dark large class="mx-2">mdi-facebook</v-icon>
                            <v-icon dark large class="mx-2">mdi-instagram</v-icon>
                            <v-icon dark large class="mx-2">mdi-linkedin</v-icon>
                        </div>
                        <div class="mt-8 ml-8">
                            <p class="text-left">
                                Fiftech Zone Private Limited is an IT company established in 2021 under the companies act 2006 with the motive to make Nepal digital.
                            </p>
                        </div>
                        <div class="px-4 d-flex align-center">
                            <img src="../static/Footer/map masked.png" height="80px" alt="">
                            <v-btn class="" rounded>CLick to view map</v-btn>    
                        </div>
                    </v-col>
                    <v-col cols="1"></v-col>
                </v-row>
            </div>
        </div>
    
    <v-footer dark>
        <div><p class="text--left" > &copy;Copyright {{ new Date().getFullYear() }} Fiftech Zone. All rights reserved.</p> </div>
    </v-footer>
</div>
    
    
</template>
<style scoped>
    .footer-main {
        /* background: transparent linear-gradient(11deg, #9B51E0 0%, #347FE2 76%, #0693E3 100%) 0% 0% no-repeat padding-box; */
    }
</style>