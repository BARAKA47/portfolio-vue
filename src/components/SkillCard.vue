<template>
  <v-container class="">
    <v-card color="rgba(100,100,100,0.5)" theme="dark" class="py-4 px-2" >
      <v-row no-gutters align="center" justify="start">
        <v-col cols='12' md='3'><v-avatar class="ma-3" size="60" rounded="0"><v-img :src="data.image"></v-img></v-avatar>
        <h1 class="poppins title ma-2">{{data.title}}</h1></v-col>
        <v-col cols='12' md='9'> 
          <v-row align="" justify="space-around">
          <div v-for="skill in data.skills" :key="skill.name">
            <v-avatar class="ma-1" size="40" rounded="0"><v-img :src="skill.image"></v-img></v-avatar>
            <p class="poppins pr">{{skill.name}}</p>
          </div>
          </v-row>
        </v-col>
      </v-row>

    </v-card>
  </v-container>
</template>

<script setup>

defineProps({
  data: Object
})

</script>
<style scoped>
.title {
  color: white !important;
  font-family: "Kaushan Script", cursive;
  font-size:1rem;
  /* font-family: Comic Sans MS, Comic Sans, cursive;; */
}
.pr{
  font-size: 0.8  rem;
  color: white !important;

}
.small{
  font-size: 0.7  rem;
  color: lightgray !important;
}
.poppins {
  font-family: 'Poppins';
  /* font-size: 1.5rem; */
  /* font-family: Comic Sans MS, Comic Sans, cursive;; */
}

</style>