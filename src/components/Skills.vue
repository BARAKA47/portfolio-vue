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
    image: "/assets/code.png",
    title:'Programming languages',
    skills:[
          {name:'Python', image:"/assets/python.png"},
          {name:'Java', image:"/assets/java.png"},
          {name:'C++', image:"/assets/cpp.png"},
          {name:'Dart', image:"/assets/dart.png"},
        ]
  },

  {
    image: "/assets/comp.png",
    title:'Backend & Cloud',
    skills:[
          {name:'AWS', image:"/assets/aws.png"},
          {name:'Django', image:"/assets/django.png"},
          {name:'FastAPI', image:"/assets/fastapi.png"},
          {name:'Docker', image:"/assets/docker.png"},
          {name:'GraphQL', image:"/assets/dart.png"},
          {name:'Git', image:"/assets/git.png"},
          {name:'Linux', image:"/assets/linux.png"},
        ]
  },

  {
    image: "/assets/phone.png",
    title:'Mobile and Frontend',
    skills:[
          {name:'Vuejs', image:"/assets/vue.png"},
          {name:'Flutter', image:"/assets/flutter.png"},
          {name:'HTML', image:"/assets/html-5.png"},
          {name:'CSS', image:"/assets/css-3.png"},
        ]
  },

  {
    image: "/assets/db.png",
    title:'Databases',
    skills:[
          {name:'MySQL', image:"src/assets/mysql.png"},
          {name:'PostgreSQL', image:"src/assets/postgres.png"},
          {name:'MongoDB', image:"src/assets/mongo.png"},
          {name:'Redis', image:"src/assets/redis.png"},
          {name:'Neo4j', image:"src/assets/neo4j.png"},
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