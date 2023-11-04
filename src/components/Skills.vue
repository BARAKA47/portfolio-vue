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
          {name:'Python', image:"/assets/skills/python.png"},
          {name:'Java', image:"/assets/skills/java.png"},
          {name:'C++', image:"/assets/skills/cpp.png"},
          {name:'Dart', image:"/assets/skills/dart.png"},
        ]
  },

  {
    image: "/assets/comp.png",
    title:'Backend & Cloud',
    skills:[
          {name:'AWS', image:"/assets/skills/aws.png"},
          {name:'Django', image:"/assets/skills/django.png"},
          {name:'FastAPI', image:"/assets/skills/fastapi.png"},
          {name:'Docker', image:"/assets/skills/docker.png"},
          {name:'GraphQL', image:"/assets/skills/dart.png"},
          {name:'Git', image:"/assets/skills/git.png"},
          {name:'Linux', image:"/assets/skills/linux.png"},
        ]
  },

  {
    image: "/assets/phone.png",
    title:'Mobile and Frontend',
    skills:[
          {name:'Vuejs', image:"/assets/skills/vue.png"},
          {name:'Flutter', image:"/assets/skills/flutter.png"},
          {name:'HTML', image:"/assets/skills/html-5.png"},
          {name:'CSS', image:"/assets/skills/css-3.png"},
        ]
  },

  {
    image: "/assets/db.png",
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