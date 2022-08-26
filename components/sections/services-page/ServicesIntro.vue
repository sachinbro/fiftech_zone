<template>
    <div >
        <v-container fluid>
            <v-row class="background">
               
                <v-col cols="6" class="mt-2 mt-sm-10 text-center white--text">
                    <p class="text-h5 text-sm-h4">Our Services</p>
                    <p class="text-caption text-sm-subtitle-1  ">We provide a wide range of professional services to meet your needs. <br  v-if="$vuetify.breakpoint.name !== 'xs'">
                    We promise to provide every service with a smile, and to your highest level of satisfaction.</p>
                </v-col>
                <v-col cols="0" sm=""></v-col>
                <v-col class="mt-0 mt-sm-10 ml-4 ml-sm-0" cols="4" sm="2"><img src="../../../static/sections/Servicespage/Image 400.png" height="300px" alt=""></v-col>
                <v-col cols="1" sm="2"></v-col>
            </v-row>
        </v-container>
    </div>
</template>
<style scoped>
    .background{
     
    
    /* background-image: url("../../../static/sections/Servicespage/background.png");
    background-repeat: no-repeat;
    background-size: 100% 100%; */
    
}
</style>