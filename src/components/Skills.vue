<template>
  <v-container>
    <v-responsive class="align-center text-center py-16">
      <h1 class="title"> Skills </h1>
      <SkillCard v-for="d in data" :key="d.title" :data="d" />
      
    </v-responsive>
  </v-container>
</template>

<script setup>
import SkillCard from '@/components/SkillCard.vue'
const data = [
  {
    image: "src/assets/code.png",
    title:'Programming languages',
    skills:[
          {name:'Python', image:"src/assets/skills/python.png"},
          {name:'Java', image:"src/assets/skills/java.png"},
          {name:'C++', image:"src/assets/skills/cpp.png"},
          {name:'Dart', image:"src/assets/skills/dart.png"},
        ]
  },

  {
    image: "src/assets/comp.png",
    title:'Backend & Cloud',
    skills:[
          {name:'AWS', image:"src/assets/skills/aws.png"},
          {name:'Django', image:"src/assets/skills/django.png"},
          {name:'FastAPI', image:"src/assets/skills/fastapi.png"},
          {name:'Docker', image:"src/assets/skills/docker.png"},
          {name:'GraphQL', image:"src/assets/skills/dart.png"},
          {name:'Git', image:"src/assets/skills/git.png"},
          {name:'Linux', image:"src/assets/skills/linux.png"},
        ]
  },

  {
    image: "src/assets/phone.png",
    title:'Mobile and Frontend',
    skills:[
          {name:'Vuejs', image:"src/assets/skills/vue.png"},
          {name:'Flutter', image:"src/assets/skills/flutter.png"},
          {name:'HTML', image:"src/assets/skills/html-5.png"},
          {name:'CSS', image:"src/assets/skills/css-3.png"},
        ]
  },

  {
    image: "src/assets/db.png",
    title:'Databases',
    skills:[
          {name:'MySQL', image:"src/assets/skills/mysql.png"},
          {name:'PostgreSQL', image:"src/assets/skills/postgres.png"},
          {name:'MongoDB', image:"src/assets/skills/mongo.png"},
          {name:'Redis', image:"src/assets/skills/redis.png"},
          {name:'Neo4j', image:"src/assets/skills/neo4j.png"},
        ]
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