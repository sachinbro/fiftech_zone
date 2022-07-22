<template>
    <div>
        <v-container class="main" fluid>
            <v-row no-gutters>
                <v-col cols="1"></v-col>
                <v-col cols="4">
                    <div class="moto mt-16 ml-5">
                        <div>GO DIGITAL,</div>
                        <div>LIVE SMART.</div>
                    </div>
                    <div class="mt-6 text--bold">
                        <div>Digitalize your business with our product services.</div>
                        <div> Let the world know where you stand in the market.</div>
                    </div>
                </v-col>
                <v-col cols="7">
                    <img src="../../../static/landing area image.svg" width="800px" height="600px" alt="" >
                </v-col>
            </v-row>
            <v-row class="d-flex justify-center" >
                <div style="font-size: 25px;" >
                    <span style="color: #B051E0; ">Learn More </span><span style="color:#ABB8C3;">about fiftech's unique features.</span>
                </div>
            </v-row>
            <v-row class="d-flex flex-column font-weight-bold justify-center align-center" >
                <div style="color:#3D2F2F; font-size: 35px;">Discover how we work</div>
                <div style="color:#3D2F2F; font-size: 35px;"> to deliver outstanding results.</div>
            </v-row>
            <v-row class="white--text">
                <v-col></v-col>
                <v-col class="tasks" cols="1">
                    <v-card elevation="0" height="" >
                        <v-card-text class=" rounded-circle text-center">
                            <div class="multilayer-circle white--text"> 
                                1
                            </div>
                        </v-card-text>
                    </v-card> </v-col>
                <v-col cols="2" class="horizontal-line"></v-col>
                <v-col cols="1">
                    <v-card-text class=" rounded-circle text-center">
                        <div class="multilayer-circle ">
                            2
                        </div>
                    </v-card-text>
                </v-col>
                <v-col cols="2" class="horizontal-line"></v-col>
                <v-col cols="1">
                    <v-card-text class=" rounded-circle text-center">
                        <div class="multilayer-circle ">
                            3
                        </div>
                    </v-card-text>
                </v-col>
                <v-col></v-col>
            </v-row>
        </v-container>
    </div>
</template>
<style scoped>
.moto{
    font: normal normal bold 50px Segoe UI;
    width: 80%;
}
.multilayer-circle{
    border-radius: 50%;
  box-shadow: 0px 0px 0px 10px rgba(155, 81, 224, 1), 0px 0px 0px 20px rgba(155, 81, 224, 0.69), 0px 0px 0px 30px rgba(155, 81, 224, 0.39);
  width: 20px;
  height:20px;
  margin: 3em;
  background-color: rgba(155, 81, 224, 1);
}
.horizontal-line{
    border-bottom: 1px solid #ABB8C3;
    height: 80px;
}

</style>