<script>
import VueSlickCarousel from "vue-slick-carousel";
import 'vue-slick-carousel/dist/vue-slick-carousel-theme.css';
import 'vue-slick-carousel/dist/vue-slick-carousel.css';
export default{
    data() {
        return {
            testimonials: [
                {
                    img: "",
                    post: "Marketing Manager",
                    name: "Luca Jacobs"
                },
                {
                    img: "",
                    post: "CEO",
                    name: "Ram Sigdel"
                }
            ],
          settings: {
            "autoplay": true,
            "edgeFriction": 0.35,
            "infinite": true,
            "speed": 500,
            "slidesToShow": 1,
            "rows": 1,
            "slidesToScroll": 1,
            "autoplaySpeed": 3000,
          },

        };
    },
    components: { VueSlickCarousel },
    methods: {
        nextSlide(){
          this.$refs.slick.next();
        },
        prevSlide(){
          this.$refs.slick.prev();
        },
    }
}

</script>
<template>
    <div>
        <v-container fluid class="mt-sm-16" id="testimonials">
            <v-row>
                <v-col cols="0" sm="1"></v-col>
                <v-col class="text-center text-md-left">
                    <div class="text-h4  font-weight-bold">Testimonials</div>
                </v-col>
            </v-row>
          
              <v-container fluid>
                <v-row>
                <v-col cols="1"></v-col>
                  <v-col cols="12" sm="6" md="4" lg="3">
                    <v-container  class="text-h5 text-center">
                      <VueSlickCarousel v-bind="settings" ref="slick">
                        <div v-for="testimonial in testimonials" :key="testimonial.name">
                          <v-card elevation="0">
                            <v-card-text class="ma-md-4">
                              <div class=" rounded-lg pa-md-10 pa-4 text-subtitle-1 testimonial">
                                <p>
                                  The best generator I could find because it optionally includes lists, formatting, blockquotes and a
                                  bunch of other HTML Pan Ipsum - Gives you the option to generate text with a lot of different word lists
                                  Bacon Ipsum - If you want to make your client hungry
                                </p>
                              </div>
                              <div class="testimonial d-flex flex-column"></div>
                              <div class="d-flex text-subtitle-1">
                                <v-avatar size="70" class="mt-2">
                                  <img src="../../../static/biralo.png" alt="">
                                </v-avatar>
  
                                <p class="mt-4 ml-4">{{testimonial.name}}<br>{{testimonial.post}}</p>
                              </div>
                            </v-card-text>
                          </v-card>
                        </div>
                      </VueSlickCarousel>
  
                    </v-container>
                  </v-col>

                  <v-col cols="0" md="2"></v-col>
                  <v-col cols="5" class="d-none d-md-block text-h3 text-center font-weight-bold mt-16">
                      <div >We use our focused set of</div>
                      <div >capabilities to build </div>
                      <div >great experiences.</div>
                      <div class="mt-2 text-h6 font-weight-light text--secondary">We are as good as they say we are.</div>
                      <div class="pa-4">
                        <v-btn elevation="0" style="border: 1px solid black;" @click="prevSlide()" class="rounded-lg mx-4" icon tile>
                          <v-icon x-large   >mdi-chevron-left</v-icon>
                        </v-btn>
                        <v-btn elevation="0" style="border: 1px solid black;" @click="nextSlide()" class="rounded-lg" icon tile>
                          <v-icon x-large  >mdi-chevron-right</v-icon>
                        </v-btn>
                     </div>
                  </v-col>
                </v-row>
              </v-container>
        </v-container>
    </div>
</template>
<style scoped>
    .testimonial{
        background-color: rgba(0,0,0,0.1);
    }

    
    
</style>
