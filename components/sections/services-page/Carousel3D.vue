<script>
import {Carousel3d, Slide } from 'vue-carousel-3d'
export default{
    components: {Carousel3d,Slide},
    data(){
        return {
            items: [
                {
                    title: 'Web Development',
                    description: 'Websites are the future of the internet. We build them with the latest technologies and we make sure that they are secure and fast.',
                    img: 'Image 17.png'
                },
                {
                    title: 'Digital Marketing',
                    description: 'Websites are the future of the internet. We build them with the latest technologies and we make sure that they are secure and fast.',
                    img: 'Image 34.png'
                },
                {
                    title: 'Graphic Design',
                    description: 'Websites are the future of the internet. We build them with the latest technologies and we make sure that they are secure and fast.',
                    img: 'Image 27.png'
                },
                {
                    title: 'IT Training ',
                    description: 'Websites are the future of the internet. We build them with the latest technologies and we make sure that they are secure and fast.',
                    img: 'Image 19.png'
                },
                {
                    title: 'Mobile Application Development',
                    description: 'Websites are the future of the internet. We build them with the latest technologies and we make sure that they are secure and fast.',
                    img: 'Image 23.png'
                },
            ]
        }
    }
    }
</script>
<template>
    <v-row class="mt-10">
        <v-col cols="1"></v-col>
        <v-col>
            <Carousel3d :controls-visible="true" 
            height="400" width="350" :border="10">
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
        </v-col>
        <v-col cols="1"></v-col>
        
    </v-row>
</template>