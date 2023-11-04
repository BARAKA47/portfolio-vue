<template>
  <v-app class="appbg">
    <v-img src="/src/assets/meteors5.gif" class="meteors" :style="{opacity: bgopacity}"></v-img>
    <v-img class="background" :style="{opacity: bgopacity}"></v-img>

    <v-container>
      <HelloWorld class="z1" />
      <v-row>
      <v-container :style="'height: 150px'"></v-container>
      </v-row>
      <v-row>
      <v-col cols='12' md='8'><Introduction/></v-col>
      <v-col cols='12' md='4'><Orbits/></v-col>
      </v-row>

      <v-row>
      <Experience class="z1"/>
      </v-row>

      <v-row>
      <Skills class="z1"/>
      </v-row>
      
      <v-row>
      <Projects class="z1"/>
      </v-row>
      <br/>
      

    </v-container>
    <v-img v-if="false" src="/src/assets/agency.png"></v-img>
    <v-img v-if="false" src="/src/assets/changdle.png"></v-img>
    <v-img v-if="false" src="/src/assets/code.png"></v-img>
    <v-img v-if="false" src="/src/assets/comp.png"></v-img>
    <v-img v-if="false" src="/src/assets/db.png"></v-img>
    <v-img v-if="false" src="/src/assets/dice.png"></v-img>
    <v-img v-if="false" src="/src/assets/dk.png"></v-img>
    <v-img v-if="false" src="/src/assets/entr.png"></v-img>
    <v-img v-if="false" src="/src/assets/laika.png"></v-img>
    <v-img v-if="false" src="/src/assets/microdeep.png"></v-img>
    <v-img v-if="false" src="/src/assets/microship.png"></v-img>
    <v-img v-if="false" src="/src/assets/otani.png"></v-img>
    <v-img v-if="false" src="/src/assets/oxygen.png"></v-img>
    <v-img v-if="false" src="/src/assets/phone.png"></v-img>
    <v-img v-if="false" src="/src/assets/random.png"></v-img>
    <v-img v-if="false" src="/src/assets/red.png"></v-img>
    <v-img v-if="false" src="/src/assets/reds.png"></v-img>
    <v-img v-if="false" src="/src/assets/rov.png"></v-img>
    <v-img v-if="false" src="/src/assets/snake.jpg"></v-img>
    <v-img v-if="false" src="/src/assets/udacity.png"></v-img>
    <v-img v-if="false" src="/src/assets/wordle.jpg"></v-img>
    <v-img v-if="false" src="/src/assets/skills/django.jpg"></v-img>
    <v-img v-if="false" src="/src/assets/skills/fastapi.jpg"></v-img>
    <v-img v-if="false" src="/src/assets/skills/dart.jpg"></v-img>
    <v-img v-if="false" src="/src/assets/skills/mysql.jpg"></v-img>
    <v-img v-if="false" src="/src/assets/skills/postgres.jpg"></v-img>
    <v-img v-if="false" src="/src/assets/skills/mongo.jpg"></v-img>
    <v-img v-if="false" src="/src/assets/skills/neo4j.jpg"></v-img>
    <v-img v-if="false" src="/src/assets/skills/redis.jpg"></v-img>
    <v-img v-if="false" src="/src/assets/skills/git.jpg"></v-img>
    <v-img v-if="false" src="/src/assets/skills/linux.jpg"></v-img>
    <v-img v-if="false" src="/src/assets/skills/dart.jpg"></v-img>
  </v-app>
</template>

<script setup>
  import DefaultView from './View.vue'
  import HelloWorld from '@/components/HelloWorld.vue'
  import Introduction from '@/components/Introduction.vue'
  import Skills from '@/components/Skills.vue'
  import Experience from '@/components/Experience.vue'
  import Orbits from '@/components/Orbits.vue'
  import Projects from '@/components/Projects.vue'

  import { ref, onMounted } from 'vue'

  const bgopacity = ref(1)

  onMounted(() => {
  window.addEventListener('scroll', onScroll);
  })

  const onScroll = (event)=>{
     var op = 1- window.scrollY / 700;
		  if ( op < 0.4) op = 0.4;
      bgopacity.value = op
  }


 
//     export default{
//     data() {
//       return{
//     bgopacity: 1
//       }
//   },
//   created () {
//     window.addEventListener('scroll', this.onScroll);
//   },
//   destroyed () {
//     window.removeEventListener('scroll', this.onScroll);
//   },
//   methods: {
//     onScroll (event) {
//       var bgopacity = 1- window.scrollY / 700;
// 		  if ( bgopacity < 0.4) bgopacity = 0.4;
//       this.bgopacity = bgopacity
//     }
//   }
// }
</script>

<style scoped>

body {
  font-weight: 400;
  font-size: 14px;
  line-height: 1.7;
  color: #000;
  background: #000;
  
}
.appbg {
  background-color: black;
}
.background {
  content: "";
  position: fixed;
  background: url(/src/assets/milky.jpg);
  background-size: cover;
  background-position:center;
  background-attachment: fixed;
  top: 0;
  left: 0;
  bottom: 0;
  right: 0;
}
.meteors{
  width: 100%;
  height: 100%;
  position: fixed;
}
</style>
