<script>
export default{
    mounted(){
        //  this.validate();
    },
    data(){
        return {
            isSubmited: false,
            jobs: [
                {
                    id: 1,
                    post: "Frontend Developer",
                    contract: "Senior level",
                    time: "Full time",
                    aboutJob: "Toptal is an exclusive network of top freelancers from around the world. Fortune 500 companies and Silicon Valley startups hire Toptal for their most important projects. Toptal is one of the fastest -growing fully remote networks and empowers freelance software developers, designers, finance ex perts, product managers, and project managers worldwide to grow and excel in their freelance caree rs. Toptal clients vary in sizes and industries, from enterprise organizations and big tech",
                    requirements: [
                        "Three or more years of experience and proven track record.",
                        "Hands-on experience creating wireframes, prototypes, storyboards, user flows, etc.",
                        "Experience using tools such as Photoshop, Sketch, Illustrator, InVision, UXPin, Quartz.",
                        "Experience with eCommerce or Landing Page Design is a bonus.",
                        "Understanding of basic front-end languages: HTML5, CSS3 Javascript.",
                        "Creative ideas with a problem solving mindset.",
                        "Experience working in an agile/scrum development process.",
                        "Be open to receiving objective criticism and improving upon it. ",
                        "Full-time availability is a strong advantage"
                    ]
                },
                {
                    id: 2,
                    post: "Backend Developer",
                    contract: "Senior level",
                    time: "Full time",
                    aboutJob: "Toptal is an exclusive network of top freelancers from around the world. Fortune 500 companies and Silicon Valley startups hire Toptal for their most important projects. Toptal is one of the fastest -growing fully remote networks and empowers freelance software developers, designers, finance ex perts, product managers, and project managers worldwide to grow and excel in their freelance caree rs. Toptal clients vary in sizes and industries, from enterprise organizations and big tech",
                    requirements: [
                        "Three or more years of experience and proven track record.",
                        "Hands-on experience creating wireframes, prototypes, storyboards, user flows, etc.",
                        "Experience using tools such as Photoshop, Sketch, Illustrator, InVision, UXPin, Quartz.",
                        "Experience with eCommerce or Landing Page Design is a bonus.",
                        "Understanding of basic front-end languages: HTML5, CSS3 Javascript.",
                        "Creative ideas with a problem solving mindset.",
                        "Experience working in an agile/scrum development process.",
                        "Be open to receiving objective criticism and improving upon it. ",
                        "Full-time availability is a strong advantage"
                    ]

                }
            ],
            valid: false,
                name: '',
                nameRules: [
                    v => !!v || 'Name is required',
                    v => (v && v.length <= 30) || 'Name must be less than 10 characters',
                ],
                email: '',
                emailRules: [
                    v => !!v || 'E-mail is required',
                    v => /.+@.+\..+/.test(v) || 'E-mail must be valid',
                ],
                phone: '',
                phoneRules: [
                    v => !!v || 'Phone is required',
                    v => /^\d{10}$/.test(v) || 'Phone must be valid',
                ],
                select: null,
                items: [
                    'Backend Developer',
                    'Frontend Developer',
                    'Full Stack Developer',
                    'React-Native Developer',
                ],
                checkbox: false,
        }
    },
    methods: {
      validate () {
        this.$refs.form.validate()
      },
      reset () {
        this.$refs.form.reset()
      },
      resetValidation () {
        this.$refs.form.resetValidation()
      },
       async submit () {
            await this.validate();
            if (this.valid) {
                this.isSubmited = true;
                console.log(this.name,this.email,this.phone, this.select, this.checkbox);
            }
        },
    },
}
</script>
<template>
<div v-if="jobs" class="ma-10">
    <div class="text-center mt-16">
        <p class="text-h5 text-sm-h4 font-weight-medium">Job Openings</p>
        <p class="text--secondary text-caption text-sm-subtitle-1">Sample text. Click to select the text box. Click again or double click to start editing the text.<br> Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.</p>
    </div>
    <div v-for="job in jobs"
    :key="job.id" class="mt-10">
       <v-row>
        <v-col></v-col>
        <v-col class="rounded-xl pl-sm-8" cols="12" sm="10" style="border: 1px solid #707070">
            <div class="d-flex">
                <ul class="text-h6 text-sm-h5"><li>{{job.post}}</li></ul>
                <span class="mx-sm-5"><v-btn elevation="0">Apply now</v-btn></span>
            </div>
            <div>
                <div class="ml-16 mt-4">
                    <v-icon>mdi-briefcase-variant</v-icon> Contract: {{job.contract}} <br>
                    <v-icon>mdi-clock </v-icon> {{job.time}}

                </div>
                
                <div class="ml-8 mt-6">
                    <p class="text-h6">About the Job</p>
                    <p class="text-subtitle-2 text--secondary" style="width: 60%;">
                        {{job.aboutJob}}
                    </p>
                    <p class="text-h6 font-weight-medium">Requirements</p>
                </div>
                <ul class="mb-2">
                    <li v-for="requirement in job.requirements" :key="requirement" class="text-body-1 ml-3">{{requirement}}</li>
                </ul>
                <p class="ml-3" style="width: 70%;">If you’re interested in pursuing an engaging career working on full-time freelance jobs for exclusive clients, take the next step by clicking apply and filling out the short form to get started.</p>
                </div>
        </v-col>
        <v-col></v-col>
       </v-row> 
           </div>
        <v-row v-if="!isSubmited" class="text-h5 font-weight-bold flex-column mt-16">
           
            <div class="text-center mb-2">Apply Now</div>
            <div class="text-h5 text-center">Add your talent and experience to our growing team!</div>
        </v-row>
        <v-row v-else></v-row>
        <v-row>
            <v-col cols="3">

            </v-col>
            <v-col v-if="!isSubmited" cols="6" class="rounded-xl  mt-8  px-10 elevation-2" style="border: 1px solid black">
                <v-form  
                        @submit="submit"
                        ref="form"
                        v-model="valid"
                        lazy-validation
                    >
                        <v-text-field
                        v-model="name"
                        :counter="30"
                        :rules="nameRules"
                        label="Full Name"
                        required
                        ></v-text-field>

                        <v-text-field
                        v-model="email"
                        :rules="emailRules"
                        label="E-mail"
                        required
                        ></v-text-field>
                        
                        <v-text-field
                        v-model="phone"
                        :rules="phoneRules"
                        label="Phone"
                        :counter="10"
                        required
                        ></v-text-field>

                        <v-select
                        v-model="select"
                        :items="items"
                        :rules="[v => !!v || 'Item is required']"
                        label="Post"
                        required
                        ></v-select>

                        <v-file-input
                        label="CV/Resume"
                        truncate-length="15"
                        ></v-file-input>

                        <v-checkbox
                        v-model="checkbox"
                        :rules="[v => !!v || 'You must agree to continue!']"
                        label="I have read and agree to the terms and conditions"
                        required
                        ></v-checkbox>

                        <v-btn
                        :disabled="!valid"
                        color="success"
                        class="mr-4"
                        @click="submit"
                        >
                        Submit
                        </v-btn>

                        <v-btn
                        color="error"
                        class="mr-4"
                        @click="reset"
                        >
                        Reset Form
                        </v-btn>
                </v-form>
            </v-col>
        <v-col v-else class="ma-16 text-h4">
            Application Registered Successfully!
        </v-col>
        <v-col cols="3"></v-col>
       </v-row>

</div>
<v-row v-else class="pa-10 justify-center">
    <p class="text-h6 text-center">Sorry, there are no recent openings. Keep in touch for more information!</p>
    <img src="../../../static/sections/Careerpage/undraw_Cancel_re_pkdm.png" height="300px" alt="">
</v-row>
</template>
<style scoped>
    .v-btn{
        text-transform: none;
        background-color:rgba(41, 50, 61, 1) !important;
        color: white !important;
    }
</style>