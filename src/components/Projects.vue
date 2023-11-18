<template>
  <v-container>
    <v-responsive class="align-center text-center py-16">
      <h1 class="title"> Selected Projects </h1>
      <v-row>
      <v-col v-for="d in data" :key="d.title" >
      <ProjectCard :data="d" />
       </v-col>
      </v-row>
      
    </v-responsive>
  </v-container>
</template>

<script setup>
import ProjectCard from '@/components/ProjectCard.vue'
const data = [
      {
        color:'#730c05',
        title: 'Red',
        subtitle: 'Software Solution',
        short: 'A Blood donation platform',
        long: 'Red is a technology platform designed to aid individuals in need of blood in locating active donors in their vicinity. We are proud to serve over 15,000 users across 25 countries, and have helped to save over 1,000 lives.',
        image: '/assets/reds.png',
        actions:[{name:'Website', to:"https://redbloodapp.com"}, {name:"Download App", to:'https://redblood.app.link'}]
      },
      
      {
        color:'#490573',
        title: 'MicroDeep',
        subtitle: 'Graduation Project',
        short: 'Automated TB diagnosis via Embedded Deep learning',
        long: 'As part of my graduation project at the Faculty of Engineering, my team and I designed and implemented an intelligent microscope using 3D printing and Embedded Deep Learning. The device is capable of automatically detecting the presence of tuberculosis (TB) in a sputum sample, while minimizing the need for human intervention.',
        image: '/assets/microdeep.png',
        actions:[{name:'Know More', to:"https://drive.google.com/file/d/17sSHDEe1qEqwJM7uStB9OHlRjk8Kai7o/view?usp=share_link"}]
      },
      
      {
        color:'#732905',
        title: 'Laika',
        subtitle: 'Platform - Under development',
        short: 'A Pet Adoption Platform',
        long: 'Laika is app for pet owners that allow users to adopt pets and share media content with other pet owners.',
        image: '/assets/laika.png',
        actions:[{name:'Demo', to:"https://redbloodapp.com/laika/index.html"}]
      },

      {
        color:'#FFBEF8',
        title: 'Wishify',
        subtitle: 'Platform - Under development',
        short: "You deserve what you wish for",
        long: "Enough perfumes? Wishify lets you create a wishlist to share with your friends, so that you can receive gifts that you actually want",
        image: '/assets/snake.jpg',
        actions:[{name:"Website", to:'https://wishify.vercel.app'}]
      },

      {
        color:'#054a73',
        title: 'Changdle',
        subtitle: 'Game',
        short: 'A Frustrating Wordle',
        long: 'A wordle-like game where the secret word changes with every wrong guess, built with ReactJS.',
        image: '/assets/changdle.png',
        actions:[{name:'Demo', to:"https://changdle.vercel.app"}, {name:"Github", to:'https://github.com/nehadyounis/Changdle'}]
      },

      {
        color:'#557305',
        title: 'Word Random API',
        subtitle: 'A free API',
        short: 'A free api for random word generation',
        long: 'Wordle Random Api is an api that is able to generate a random word or a set of random words according to your criteria. Currently supported language is English. The api uses a dataset of more than 350,000 English words, of which 3000 words were marked as common words for daily use.',
        image: '/assets/random.png',
        actions:[{name:'Demo', to:"https://wordle-random-api-demo.vercel.app"}, {name:'Github', to:"https://github.com/nehadyounis/wordle_random_api"}]
      },

      {
        color:'#137305',
        title: "Wordle Analysis",
        subtitle: 'Data analysis',
        short: 'What is the best word to start wordle with?',
        long: "\"Rocky\"? \"Fluid\"? Maybe \"Hurry\"? Let's use python to find out what is the best word among all the words to start Wordle with!",
        image: '/assets/wordle.jpg',
        actions:[{name:"Github", to:'https://github.com/nehadyounis/wordle_best_words'}]
      },

      {
        color:'#057324',
        title: 'Dar El Kawthar App',
        subtitle: 'Software Solution',
        short: 'A school management app',
        long: 'An app that connect between the teacher and the parent to make sure education is going as it should',
        image: '/assets/dk.png',
        actions:[{name:'View on Google Play', to:"https://play.google.com/store/apps/details?id=com.nehad.darelkawthar&hl=ar&gl=US"}]
      },

      {
        color:'#053173',
        title: 'Vlinder',
        subtitle: 'A College Embedded Project',
        short: 'An ROV for MATE competition ',
        long: 'Vlined is an ROV capable of performing underwater complex applictaions',
        image: '/assets/rov.png',
        actions:[]
      },
      {
        color:'#730562',
        title: 'Pixeled Snake',
        subtitle: 'Embedded Systems',
        short: "Snake on VGA screen",
        long: "Who doesn't like snake? today we're building snake on an arduino, and conneting it to a vga monitor directly! without any modules!",
        image: '/assets/snake.jpg',
        actions:[{name:"Github", to:'https://github.com/nehadyounis/Snake-on-Arduino'}]
      },
      
]

</script>
<style scoped>
.title {
  color: white !important;
  font-family: 'Poppins';
  font-size:3rem;
}
.poppins {
  color: white !important;
  font-family: 'Poppins';
  font-size: 1.5rem;
}

</style>