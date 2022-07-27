<script>
    export default {
        data(){
            return {
                primaryValues: [
                    {
                        title: 'Integrity',
                        description: 'There are many variations of lorem duos lora spassages of Lorem Ipsum available internet tend to repeat predefined.',
                        img: 'Image 6.png',
                        
                    },
                     {
                        title: 'Accountability',
                        description: 'There are many variations of lorem duos lora spassages of Lorem Ipsum available internet tend to repeat predefined.',
                        img: 'Image 7.png',
                        
                    },
                    {
                        title: 'Diligence',
                        description: 'There are many variations of lorem duos lora spassages of Lorem Ipsum available internet tend to repeat predefined.',
                        img: 'Image 8.png',
                        
                    },
                    {
                        title: 'Perseverance',
                        description: 'There are many variations of lorem duos lora spassages of Lorem Ipsum available internet tend to repeat predefined.',
                        img: 'Image 13.png',
                    },
                    {
                        title: 'Discipline',
                        description: 'There are many variations of lorem duos lora spassages of Lorem Ipsum available internet tend to repeat predefined.',
                        img: 'Image 10.png',
                    }
                    
                ]
            }
        }
    }
</script>
<template>
    <div class="mt-16" >
        <p class="text-h6 text-center">FIVE PRIMARY VALUES OF FIFTECHZONE</p>
        <p class="text-center text--disabled">There are many variations of lorem passages of Lorem Ipsum available, but <br> the majority have suffered. All the Lorem Ipsum generators.</p>
        <v-row>
            <v-col>

            </v-col>
            <v-col cols="6">
                <v-timeline>
                <v-timeline-item 
                v-for="value in primaryValues"
                :key="value.title"
                small>
                    <img :src="require(`../../../static/sections/Aboutpage/${value.img}`)" height="250px" alt="" >
                    <template v-slot:opposite>
                        <v-card elevation="0">
                            <v-card-title>{{value.title}}</v-card-title>
                            <v-card-text>
                                {{value.description}}
                            </v-card-text>
                        </v-card>
                    </template>
                </v-timeline-item>
            </v-timeline>
            </v-col>
            <v-col></v-col>
        </v-row>
        
    </div>
</template>