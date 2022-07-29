<script>
export default{
    data(){
        return {
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
            ]
        }
    }
}
</script>
<template>
<div class="ma-10">
    <div class="text-center mt-16">
        <p class="text-h6 font-weight-semibold">Job Openings</p>
        <p class="text--secondary text-subtitle-1">Sample text. Click to select the text box. Click again or double click to start editing the text.<br> Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.</p>
    </div>
    <div v-for="job in jobs"
    :key="job.id" class="mt-10">
       <v-row>
        <v-col></v-col>
        <v-col class="rounded-xl pl-8" cols="10" style="border: 1px solid #707070">
            <div class="d-flex">
                <ul class="text-h5"><li>{{job.post}}</li></ul>
                <span class="mx-5"><v-btn elevation="0">Apply now</v-btn></span>
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
</div>
</template>
<style scoped>
    .v-btn{
        text-transform: none;
        background-color:rgba(41, 50, 61, 1) !important;
        color: white !important;
    }
</style>