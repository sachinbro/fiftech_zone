<template>
            <v-row class="mt-10 pa-4 pa-sm-0">
                <v-col cols="0" sm="1" md="2"></v-col>
                <v-col >
                    <v-card max-width="600px" :class="$vuetify.breakpoint.name === 'xs' ? '': 'vision'" elevation="5">
                    <v-card-title class="justify-center ">
                        Our vision
                    </v-card-title>
                    <div class="d-flex justify-center">
                        <img
                        height="200px"
                        src="../../../static/sections/Aboutpage/Image 11.png"
                        />
                    </div>
                    <v-card-text>
                        <p class="px-4">To continuously experiment and progress toward intelligent software and applications with the implementation of Artificial Intelligence to meet people's needs.</p>
                    </v-card-text>
                </v-card>
                </v-col>
                <v-col cols="0" sm="1">
                </v-col>
                 <v-col>
                    <v-card max-width="600px" elevation="8" :class="$vuetify.breakpoint.name === 'xs' ? '' : 'mission'">
                    <v-card-title class="justify-center">
                        Our Mission
                    </v-card-title>
                    <div class="d-flex justify-center">
                        <img
                            height="200px"
                            src="../../../static/sections/Aboutpage/Image 12.png"
                            />
                    </div>
                    <v-card-text>
                        <p class="px-4">To continuously experiment and progress toward intelligent software and applications with the implementation of Artificial Intelligence to meet people's needs.</p>
                    </v-card-text>
                </v-card>
                </v-col>
                <v-col cols="0" sm="1" md="2"></v-col>
            </v-row>
</template>
<style scoped>
.vision:hover{
    animation: transform 0.5s forwards;

    
}
.mission:hover{
    animation: transform1 0.5s forwards;
}
@keyframes transform {
        0%{
            right: 0px;
        }
        50%, 100%{
            right: -50px;
        }
    }
@keyframes transform1 {
        0%{
            left: 0px;
        }
        50%, 100%{
            left: -50px;
        }
    }
</style>