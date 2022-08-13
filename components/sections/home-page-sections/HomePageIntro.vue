<script>
export default{
    computed: {
      screen () {

        switch (this.$vuetify.breakpoint.name) {
          case 'xs': return 'small'
          case 'sm': return 'small'
          default : return 'large'
        }
      },
    },

}
</script>
<template>
<div>
        <v-container  fluid class="mt-n1">
            <v-row  :class="(screen === 'small') ?  'smallbackground' : 'background'">
                <!-- <v-col cols="1" class="hidden-sm-and-down"></v-col> -->
                <v-col cols="6" lg="6" md="6" align="center" class="white--text">
                    <div class="hidden-sm-and-down text-h2 font-weight-medium mt-16 ml-sm-5">
                        <div>GO DIGITAL,</div>
                        <div>LIVE SMART.</div>
                    </div>
                    <div class="hidden-md-and-up text-h4 font-weight-medium mt-16 ml-sm-5">
                        <div>GO DIGITAL,</div>
                        <div>LIVE SMART.</div>
                    </div>
                    <div class="mt-0 mt-sm-6 text-h6 text--bold">
                        <div>Digitalize your business with our product services.</div>
                        <div> Let the world know where you stand in the market.</div>
                    </div>
                </v-col>
                <v-col cols="6" class="hidden-sm-and-down">
                    <img class="hidden-sm-and-down" src="../../../static/landing area image.svg" width="800px" height="600px" alt="" >
                </v-col>
                <v-col class="hidden-md-and-up" cols="6">
                    <v-img  :src="require('../../../static/landing area image.svg')" aspect-ratio="2" height="400" width="600" alt="" > </v-img>
                </v-col>
            </v-row>
            <v-row class="d-none d-sm-flex  justify-center" >
                <div style="font-size: 25px;" >
                    <span style="color: #B051E0; ">Learn More </span><span style="color:#ABB8C3;">about fiftech's unique features.</span>
                </div>
            </v-row>
            <v-row class="d-none d-sm-flex flex-column font-weight-bold text-h4 justify-center align-center" >
                <div style="color:#3D2F2F; ">Discover how we work</div>
                <div style="color:#3D2F2F; "> to deliver outstanding results.</div>
            </v-row>
            <v-row class="white--text  d-none d-sm-flex justify-space-around" >
                <v-col cols="1"></v-col>
                <v-col class="tasks mt-2" cols="1">
                        <div class="hoverEffect text-center">
                            <div class="multilayer-circle font-weight-bold white--text"> 
                                1
                            </div>
                        </div>
                
                </v-col>
                <v-col cols="3" class="horizontal-line"></v-col>
                <v-col cols="1" >
                    <div class=" text-center font-weight-bold hoverEffect">
                        <div class="multilayer-circle ">
                            2
                        </div>
                    </div>
                </v-col>
                <v-col cols="3" class="horizontal-line"></v-col>
                <v-col cols="1">
                    <div class="   text-center font-weight-bold  hoverEffect">
                        <div class="multilayer-circle ">
                            3
                        </div>
                    </div>
                </v-col>
                <v-col cols="2"></v-col>
            </v-row>
            <v-row class="d-none d-sm-flex  mt-n8">
                <v-col class="d-flex flex-column align-center  text-caption ">
                    <div class="text-subtitle-1">Developing an effective strategy</div>
                    <div>Five stages of progress: setting goals or objectives, analysis,</div>
                    <div>strategy formation, strategy implementation, and strategy monitoring.</div>
                </v-col>
                <v-col class="d-flex flex-column align-center  text-caption">
                    <div class="text-subtitle-1">Software development process</div>
                    <div>We employ 5 phases of software development process:</div>
                    <div>research, ideation, design, development and iteration.</div>
                </v-col>
                <v-col class="d-flex flex-column align-center  text-caption mr-n12">
                    <div class="text-subtitle-1">Automated testing and support</div>
                    <div>Automate some repetitive but necessary tasks in formalized</div>
                    <div>testing process already in place.  </div>
                </v-col>
                <v-col cols="1"></v-col>
            </v-row>
            <v-row class="d-flex d-sm-none">
                <v-col class="tasks d-flex flex-column align-center justify-center" cols="12" >
                    <v-card elevation="0" height="">
                        <v-card-text class=" rounded-circle  text-center">
                            <div class="multilayer-circle white--text"> 
                                1
                            </div>
                        </v-card-text>
                    </v-card> 
                </v-col>
               
            </v-row>
            <v-row class="d-flex d-sm-none">
                <v-col class="d-flex flex-column align-center justify-center text-caption  mt-n7">
                    <div class="text-subtitle-1">Developing an effective strategy</div>
                    <div>Five stages of progress: setting goals or objectives, analysis,</div>
                    <div>strategy formation, strategy implementation, and strategy monitoring.</div>
                </v-col>
            </v-row>
            <v-row class="d-flex d-sm-none">
                <v-col class="tasks d-flex flex-column align-center justify-center" cols="12" >
                    <v-card elevation="0" height="">
                        <v-card-text class=" rounded-circle  text-center">
                            <div class="multilayer-circle white--text"> 
                                2
                            </div>
                        </v-card-text>
                    </v-card> 
                </v-col>
               
            </v-row>
            <v-row class="d-flex d-sm-none">
                <v-col class="d-flex flex-column align-center justify-center text-caption  mt-n7">
                    <div class="text-subtitle-1">Software development process</div>
                    <div>We employ 5 phases of software development process:</div>
                    <div>research, ideation, design, development and iteration.</div>
                </v-col>
            </v-row>
            <v-row class="d-flex d-sm-none">
                <v-col class="tasks d-flex flex-column align-center justify-center" cols="12" >
                    <v-card elevation="0" height="">
                        <v-card-text class=" rounded-circle  text-center">
                            <div class="multilayer-circle white--text"> 
                                3
                            </div>
                        </v-card-text>
                    </v-card> 
                </v-col>
               
            </v-row>
            <v-row class="d-flex d-sm-none">
                <v-col class="d-flex flex-column align-center justify-center text-caption  mt-n7">
                     <div class="text-subtitle-1">Automated testing and support</div>
                    <div>Automate some repetitive but necessary tasks in formalized</div>
                    <div>testing process already in place.  </div>
                </v-col>
            </v-row>
        </v-container>
        </div>

    
</template>
<style scoped>
.smallbackground{
    height: 50vh;
    
    background-image: url("../../../static/sections/mobile.png");
    background-repeat: no-repeat;
    background-size: 100% 100%;
    background-position: center;
    background-origin: content-box;
}
.background{
    height: 100vh;
    
    background-image: url("../../../static/sections/masked1.png");
    background-repeat: no-repeat;
    background-size: 100% 100%;
    background-position: center;
    background-origin: content-box;
}
.moto{
    font: normal normal bold 50px Segoe UI;
    width: 80%;
}
.multilayer-circle{
  border-radius: 50%;
  box-shadow: 0px 0px 0px 10px rgba(155, 81, 224, 1), 0px 0px 0px 20px rgba(155, 81, 224, 0.69), 0px 0px 0px 30px rgba(155, 81, 224, 0.39);
  width: 30px;
  height:30px;
  margin: 3em;
  background-color: rgba(155, 81, 224, 1);
}
 .hoverEffect:hover{
    animation: scale 0.5s forwards;
}
.horizontal-line{
    border-bottom: 1px solid #ABB8C3;
    height: 80px;
}


@keyframes scale {
    0% {
        transform: scale(1);
    }
    50% {
        transform: scale(1.2);
    }
    100% {
        transform: scale(1.2);
    }
    
}

</style>