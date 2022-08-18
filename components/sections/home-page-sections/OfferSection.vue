<script>
export default {
    computed: {
      height () {
        switch (this.$vuetify.breakpoint.name) {
          case 'xs': return 200
          case 'sm': return 200
          case 'md': return 100
          case 'lg': return 100
          case 'xl': return 100
        }
      },
    },
    }
</script>
<template>
    <v-container class="mt-0 mt-md-16">
        <v-row class="d-flex justify-center text-h6 text-md-h4  font-weight-bold ml-md-n16">
            What We Offer
        </v-row>
        <v-card class="mt-2 mt-sm-10  rounded-xl" elevation="3">
            <v-row> 
                    <v-col cols="12" align="center" lg="6" md="6">
                        
                        <v-row no-gutters align="center">
                            <v-col cols="2" md="4" class="pa-1 pa-md-0 ml-md-n4 ml-md-0 ml-sm-n16 ">
                                <img src="../../../static/sections/Homepage/offering2.svg" :height="$vuetify.breakpoint.name === 'xs' ? '60px' : '150px'"  alt="">
                            </v-col>
                        <v-col cols="10" md="8" class="d-flex flex-column justify-center align-center text-caption ml-lg-n10">
                            <div class="text-subtitle-1 text-md-h6 font-weight-medium font-weight-md-bold">Guarantee of Quality</div> 
                            <div>We assure quality and client satisfaction</div>                          
                            <div class="ml-md-2">and offer primarily to the paying clients who have purchased our services</div>                          
                        </v-col>
                        </v-row>
                        
                    </v-col>
                    <v-divider vertical></v-divider>
                    <v-col cols="12" lg="6" md="6" >
                        <v-row no-gutters class=" ml-md-8" align="center">
                            <v-col cols="2" md="4" class="mt-4 mt-md-0">
                            <img src="../../../static/sections/Homepage/offering1.svg"  :height="$vuetify.breakpoint.name === 'xs' ? '60px' : '150px'"  alt="">
                        </v-col>
                        <v-col cols="10" md="8" class="d-flex flex-column justify-center align-center text-caption ml-lg-n10">
                            <div class="text-subtitle-1 text-md-h6 font-weight-medium font-weight-md-bold">Planning Information</div> 
                            <p>We think regarding the activities required to achieve a  desired goal based on foresight, the fundamental capacity for mental time travel.</p>                          
                        </v-col>
                        </v-row>
                    </v-col>
                
            </v-row>
        </v-card>
        <v-row class="mt-16 text-subtitle-1 font-weight-bold text--disabled">
                <v-col cols="12" md="4" lg="4" style="color:#6E6A6A;" class="mt-14">
                    <div class="d-flex flex-column align-center">
                        <img src="../../../static/sections/Homepage/IT specialist 2.png" :height="height" alt="">
                        <div class="text--disabled">Skilled IT Specialists</div>
                    </div>
                    <div class="d-flex flex-column align-center mt-8">
                        <img src="../../../static/sections/Homepage/market analysis 2.png" :height="height"  alt="">
                        <div class="text--disabled">Market Analysis</div></div>
                    <div class="d-flex flex-column align-center mt-8">
                        <img src="../../../static/sections/Homepage/web solution 2.png" :height="height"  alt="">
                        <div class="text--disabled">Web Solutions</div></div>
                </v-col>
                <v-col cols="12" md="4" class="d-flex flex-column align-center">
                    <img src="../../../static/sections/Homepage/offering-app.png" height="550px" weight="250px" />
                </v-col>
                <v-col cols="12" md="4" style="color:#6E6A6A;" class="mt-14">
                    <div class="d-flex flex-column align-center ">
                        <img src="../../../static/sections/Homepage/planning 2.png" :height="height"  alt="">
                        <div class="text--disabled">Planning Settings</div>
                    </div>
                    <div class="d-flex flex-column align-center  mt-8">
                        <img src="../../../static/sections/Homepage/financial advice 2.png" :height="height"  alt="">
                        <div class="text--disabled">Financial Advice</div></div>
                    <div class="d-flex flex-column align-center mt-8">
                        <img src="../../../static/sections/Homepage/ideas2.png" :height="height"  alt="">
                        <div class="text--disabled">Awesome Ideas</div></div>
                </v-col>
            
        </v-row>
    </v-container>
</template>