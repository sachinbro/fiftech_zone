<script>
    import RadialProgressBar from 'vue-radial-progress'

        export default {
        data () {
            return {
            completedSteps: 10,
            totalSteps: 100,
            totalProject: 0,
            customerSatisfaction: 0,
            isIntersection: false
            }
        },

        components: {
            RadialProgressBar
        },
        methods: {
            initiateAnimation(){
                this.completedSteps = 50;
                this.totalProject = 50;
            },
            initiateAnimationCustomer(){
                this.customerSatisfaction = 100;
            },
            onIntersect(entries){
                const animate = setTimeout(()=> {
                    this.initiateAnimation()
                    this.initiateAnimationCustomer()
                }, 2000);
                this.isIntersection = entries[0].isIntersecting;
                if(!this.isIntersection){
                    this.completedSteps = 0;
                    this.customerSatisfaction = 0;
                    return
                }   
                
            }
        }
        }
</script>
<template>
    <v-row class="projectinfo pa-4">
        <v-col cols="1"></v-col>
        <v-col class=" white--text text-h3 font-weight-bold">
            <div class="d-none d-sm-block">We deliver the</div>
            <div class="d-none d-sm-block">SOFTWARE you need,</div>
            <div class="d-none d-sm-block">no more, no less.</div>
            <v-row class="text-subtitle-1" >
                <v-col>
                    <div @click="initiateAnimation()" >
                        <radial-progress-bar :diameter="150"
                        innerStrokeColor=""
                        startColor="white"
                        stopColor="white"
                       :completed-steps="completedSteps"
                       :total-steps="totalSteps"
                       class="progress-bar"
                       >
                    
                    </radial-progress-bar>
                    </div>
                    <span v-intersect="onIntersect"></span>
                    Completed {{totalProject}} + projects
                </v-col>
                <v-col>
                     <div @click="initiateAnimationCustomer()">
                        <radial-progress-bar :diameter="150"
                        innerStrokeColor=""
                        startColor="white"
                        stopColor="white"
                       :completed-steps="customerSatisfaction"
                       :total-steps="100"
                       class="progress-bar"
                       >
                    
                    </radial-progress-bar>
                    </div>
                    {{customerSatisfaction}}% customer satisfaction
                </v-col>
            </v-row>
        </v-col>
        <v-col class="d-sm-flex d-none  justify-end">
            <img src="../../../static/sections/Homepage/banner_img.png" height="500px" width="500px" alt="">
        </v-col>
        <v-col cols="1"></v-col>
    </v-row>
</template>
<style scoped>
    .projectinfo{
         background: transparent linear-gradient(10deg, #9B51E0 0%, #347FE2 76%, #0693E3 100%) 0% 0% no-repeat padding-box;
    }
    .progress-bar{
        border-radius: 50%;
        box-shadow: inset 0px 3px 15px #FFFFFF8C, 0px 3px 99px #00000052;
    }
</style>