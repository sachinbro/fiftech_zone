<script>
    export default{
        data(){
            return {
                professionals: [
                    {
                        name: 'Sanjay Chaudhary',
                        post: 'CEO',
                        description: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit.',
                        img: 'Component 53 – 1.png'
                    },
                    {
                        name: 'Pashupati Sah',
                        post: 'CTO',
                        description: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit.',
                        img: 'Component 53 – 1.png'
                    },
                    {
                        name: 'Lalit Sah',
                        post: 'Backend Developer',
                        description: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit.',
                        img: 'Component 53 – 1.png'
                    }
                ]
            }
        }
    }
</script>
<template>
    <div class="mt-14 background">
        <div class="pt-10">
            <p class="text-center text-h4"> MEET OUR TEAM <br> THE PROFESSIONALS</p> 
            <p class="text-center"> Lorem, ipsum dolor sit amet consectetur adipisicing elit. Unde, ipsam?</p>
            <v-row class="mt-16 d-flex justify-center ">
               <v-col cols="1"></v-col>
                <v-col cols="3" class="d-flex flex-column justify-center align-center mt-4"
                v-for="(professional, index) in professionals"
                :key="index"
                >
                    <v-avatar size="200"><img :src="require(`../../../static/sections/Aboutpage/${professional.img}`)" alt=""></v-avatar>
                    <p class="text-center text-h6">{{professional.name}} <br>{{professional.post}}</p>
                    <p class="text-caption-1">Lorem ipsum dolor sit amet consectetur, <br> adipisicing elit.</p>
                    <div class="d-flex justify-center">
                        <v-icon class="mx-2">mdi-facebook</v-icon>
                         <v-icon class="mx-2">mdi-instagram</v-icon>
                         <v-icon class="mx-2">mdi-linkedin</v-icon>
                         <v-icon class="mx-2">mdi-twitter</v-icon>
                        </div>
                    
                </v-col>
                <v-col cols="1"></v-col>
                
            </v-row>
        </div>
    </div>
</template>
<style scoped>
.background{
    height: 100vh;
    background-image: url("../../../static/sections/Aboutpage/teammember.png");
    background-repeat: no-repeat;
    background-size: 100% 100%;
    background-position: center;
    background-origin: content-box;
}
</style>