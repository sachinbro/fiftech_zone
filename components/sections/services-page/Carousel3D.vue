<script>
// import {Carousel3d, Slide } from 'vue-carousel-3d'
let Carousel3d, Slide = null;
if(process.client){
  Carousel3d = require('vue-carousel-3d').Carousel3d;
  Slide = require('vue-carousel-3d').Slide;
};
export default{
    components: {Carousel3d,Slide},
    data(){
        return {
            currentIndex: 0,

            items: [
                {
                    title: 'Web Development',
                    description: 'Websites are the future of the internet. We build them with the latest technologies and we make sure that they are secure and fast.',
                    img: 'Image 17.png',
                    plansTitle: 'Our Plans for Web Development',
                    plans:[
                        "All package includes domain and hosting charges. (terms applicable)",
                        "Annual maintenance chage (AMC) is 15% excluding domain and hosting renewal charge with applicable inflation rate.",
                        "AMC charge is free to additional 1 year. (promotional offer*)",
                        "ALl the prices are exclusive of taxes."
                    ]

                },
                {
                    title: 'Digital Marketing',
                    description: 'Websites are the future of the internet. We build them with the latest technologies and we make sure that they are secure and fast.',
                    img: 'Image 34.png',
                    plansTitle: "Our Plans for Digital marketing",
                    plans: [
                        "There are numerous features in a mobile apps. The cost of mobile app development varies with respect to its requirements. It is beeter to find cost of mobile app development by discussing about it's features and other requirements."
                    ]
                },
                {
                    title: 'Graphic Design',
                    description: 'Websites are the future of the internet. We build them with the latest technologies and we make sure that they are secure and fast.',
                    img: 'Image 27.png',
                    plansTitle: "Our Plans for Graphic Desgning",
                    plans: [
                        "There are numerous features in a mobile apps. The cost of mobile app development varies with respect to its requirements. It is beeter to find cost of mobile app development by discussing about it's features and other requirements."

                    ]
                },
                {
                    title: 'IT Training ',
                    description: 'Websites are the future of the internet. We build them with the latest technologies and we make sure that they are secure and fast.',
                    img: 'Image 19.png',
                    plansTitle: 'Our Plans for IT Training',
                    plans: [
                        "There are numerous features in a mobile apps. The cost of mobile app development varies with respect to its requirements. It is beeter to find cost of mobile app development by discussing about it's features and other requirements."
                    ]
                },
                {
                    title: 'Mobile Application Development',
                    description: 'Websites are the future of the internet. We build them with the latest technologies and we make sure that they are secure and fast.',
                    img: 'Image 23.png',
                    plansTitle: "Our Plans for Mobile Application Development",
                    plans:[
                        "There are numerous features in a mobile apps. The cost of mobile app development varies with respect to its requirements. It is beeter to find cost of mobile app development by discussing about it's features and other requirements."
                    ]
                },
            ]
        }
    },
    methods:{
        afterChange(index){
            console.log('afterChange', index);
            this.currentIndex = index;

        }
    },
    computed:{
        currentSlide(){
            return this.items[this.currentIndex]
        }
    }
    }
</script>
<template>
<div>
        <p class="text-h5 text-sm-h4 text-center font-weight-medium"><span style="border-bottom: 3px solid #707070">What we offer</span></p>
       <v-row class=" mt-sm-10">
        <v-col cols="1"></v-col>
        <v-col>
            <client-only>
                <Carousel3d :controls-visible="true" 
                class=""
                @after-slide-change="afterChange"
                height="400" width="350" :border="10" space="270">
                <Slide 
                class="white elevation-10 rounded-lg"
                v-for="(item, index) in items"
                :key="item.title"
                :index="index">
                    <figure>
                        <p class="text-center font-weight-bold">{{item.title}}</p>
                        <img class="px-16" :src="require(`../../../static/sections/Servicespage/${item.img}`)" height="220px" alt="" />
                        <figcaption class="text-caption px-3 text--secondary">Web developers create and maintain websites. They are also responsible for the site's technical aspects, such as
                             its performance and capacity, which are measures of a website's speed and how much traffic the site can handle.
                              In addition, web developers may create content for the site.
                        </figcaption>
                    </figure>
                </Slide>
            </Carousel3d>
            </client-only>
        </v-col>
        <v-col cols="1"></v-col>
        
    </v-row>
    <v-row class="my-sm-10">
                <v-col cols="2" sm="4"></v-col>
                <v-col cols="8" sm="6">
                    <p class="text-h6 text-md-h4 text-left">{{currentSlide.plansTitle}}</p>
                    <ul class="text-left text-caption text-sm-subtitle-2 font-weight-light text--secondary">
                    <li v-for="plan in currentSlide.plans" :key="plan.title"> {{plan}} </li>
                    </ul>
                </v-col>
                <v-col cols="2"></v-col>
            </v-row>
</div>
 
</template>
<style scoped>
.carousel-3d-container{
    height: 440px !important;
}
</style>