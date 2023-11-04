<template>
  <v-container class="">
    <v-card :color="data.color" theme="dark" class="py-8 px-2" >
      <v-row no-gutters align="start" justify="start">
        <v-col cols='12' md='2'><v-avatar class="ma-3" size="125" rounded="0"><v-img :src="data.image"></v-img></v-avatar></v-col>
        <v-col cols='12' md='8'>
          <v-row no-gutters align="center" justify="space-around">
            <v-col cols=12 md =4> <h1 class="poppins title ma-2">{{data.company}}</h1></v-col>
            <v-col cols=12 md =4><p class='poppins small'>{{data.title}}</p></v-col>
            <v-col cols=12 md =4><p class='poppins small'>{{data.date}}</p></v-col>
          </v-row>
          <v-row no-gutters align="center" justify="start">
          <v-col><p class="poppins pr text-justify" v-html="data.disc"></p></v-col>
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
  font-size:1.5rem;
  /* font-family: Comic Sans MS, Comic Sans, cursive;; */
}
.pr{
  font-size: 0.9  rem;
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