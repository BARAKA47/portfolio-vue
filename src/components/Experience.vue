<template>
  <v-container>
    <v-responsive class="align-center text-center py-16">
      <h1 class="title">Experience</h1>
      <ExperienceCard v-for="exp in data" :key="exp.name" :data="exp" />
    </v-responsive>
  </v-container>
</template>

<script setup>
import ExperienceCard from '@/components/ExperienceCard.vue'
const data = [
{image: "/src/assets/otani.png", color:"rgba(108,0,73,0.4)", company: "Otani Tradin FZCO", title:"Fullstack Software Engineer", date:"Sep 2023 - Present | Dubai, UAE", disc: "• Building and scaling FMI; an e-commerce platform for international flower trading."},
{image: "/src/assets/udacity.png", color:"rgba(34,165,223,0.4)", company: "Udacity", title:"Session Lead", date:"Sep 2022 - Nov 2023", disc:"• Facilitated group discussions and provided support to help 8000+ Udacity students achieve their learning goals while experiencing modern IT and AI concepts."},
{image: "/src/assets/red.png", color:"rgba(228,35,60,0.4)", company: "Red", title:"Founder | Software Engineer", date:"Apr 2019 - Jun2022", disc:"• Founded Red, which is a technology platform designed to aid patients in need of blood in locating active donors in their vicinity.<br/>• Scaled the app to serve +15,000 users across 25 countries. Helped to save +1,000 lives.<br>• Implemented the technical infrastructure to serve business needs.<br>• Secured seed investment funding based on a one-year valuation of 1.4M EGP.<br>• Managed a team of 6 employees."},
{image: "/src/assets/agency.png", color:"rgba(100,100,100,0.4)", company: "Egyptian Space Agenct", title:"Machine Learning Intern", date:"Jun 2021 - Sep 2021", disc:"• I worked on a project predicting the behavior of the Egysat1 satellite using time series machine learning models, including ARMA, ARIMA, MLP and RNN. Through this experience, I gained a deep understanding of the challenges and importance of data-driven decision-making in the field of space exploration, while learning alot about machine learning and deep learning."},
{image: "/src/assets/oxygen.png", color:"rgba(24,72,122,0.4)", company: "Oxygen", title:"Software Engineer", date:"Apr 2019 - Mar 2020", disc:"• Developed software solutions especially mobile apps,like a school management app, and a doctor appointment reservation app.<br>• Scaled software systems to serve 10,000 daily active users."},
]

</script>
<style scoped>
.title {
  color: white !important;
  font-family: 'Poppins';
  font-size:3rem;
  /* font-family: Comic Sans MS, Comic Sans, cursive;; */
}
.poppins {
  color: white !important;
  font-family: 'Poppins';
  font-size: 1.5rem;
  /* font-family: Comic Sans MS, Comic Sans, cursive;; */
}
</style>
