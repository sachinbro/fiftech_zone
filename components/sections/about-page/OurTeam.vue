<script>
    export default{
        data(){
            return {
                professionals: [
                    {
                        name: 'Sanjay Chaudhary',
                        post: 'CEO',
                        description: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit.',
                        img: 'biralo.png'
                    },
                    {
                        name: 'Pashupati Sah',
                        post: 'CTO',
                        description: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit.',
                        img: 'biralo.png'
                    },
                    {
                        name: 'Lalit Sah',
                        post: 'Backend Developer',
                        description: 'Lorem ipsum dolor sit amet consectetur, adipisicing elit.',
                        img: 'biralo.png'
                    }
                ]
            }
        }
    }
</script>
<template>
    <div class="ma-14">
            <p class="text-center text-h4"> MEET OUR TEAM <br> THE PROFESSIONALS</p> 
            <p class="text-center"> Lorem, ipsum dolor sit amet consectetur adipisicing elit. Unde, ipsam?</p>
            <v-row >
                <v-col></v-col>
                <v-col cols="2" class="d-flex flex-column justify-center mr-16"
                v-for="(professional, index) in professionals"
                :key="index"
                >
                    <v-avatar size="200"><img :src="require(`../../../static/${professional.img}`)" alt=""></v-avatar>
                    <p class="text-center text-h6">{{professional.name}} <br>{{professional.post}}</p>
                    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit.</p>
                    <div class="d-flex justify-center">
                        <v-icon class="mx-2">mdi-facebook</v-icon>
                         <v-icon class="mx-2">mdi-instagram</v-icon>
                         <v-icon class="mx-2">mdi-linkedin</v-icon>
                         <v-icon class="mx-2">mdi-twitter</v-icon>
                        </div>
                    
                </v-col>
                
                <!-- <v-col cols="2">
                    <v-avatar size="200" class="justify-center"><img src="../../../static/biralo.png" alt=""></v-avatar>
                    <p class="text-center text-h6">Sanjay Chaudhary <br>CEO</p>
                    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit.</p>
                </v-col>
                
                <v-col cols="2">
                    <v-avatar size="200" class="justify-center"><img src="../../../static/biralo.png" alt=""></v-avatar>
                    <p class="text-center text-h6">Sanjay Chaudhary <br>CEO</p>
                    <p>Lorem ipsum dolor sit amet consectetur, adipisicing elit.</p>
                </v-col> -->
                <v-col></v-col>
            </v-row>
    </div>
</template>