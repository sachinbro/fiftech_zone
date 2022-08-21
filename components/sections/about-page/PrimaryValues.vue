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
            <v-col cols="12" md="6">
                <v-timeline :dense="$vuetify.breakpoint.smAndDown">
                <v-timeline-item 
                v-for="value in primaryValues"
                :key="value.title"
                small
                >
                    <img slot="opposite" :src="require(`../../../static/sections/Aboutpage/${value.img}`)" :height="$vuetify.breakpoint.name === 'xs' ? '150px' : '250px'" alt="" >
                        <v-card elevation="0" >
                            <v-card-title class="text-subtitle-1 text-sm-h6">{{value.title}}</v-card-title>
                            <v-card-text class="text-caption text-sm-body-2">
                                {{value.description}}
                            </v-card-text>
                        </v-card>
                    
                </v-timeline-item>
            </v-timeline>
            </v-col>
            <v-col></v-col>
        </v-row>
        
    </div>
</template>
<style scoped>

</style>