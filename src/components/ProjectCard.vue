<template>
  <v-container class="">
    <v-card
    :color="data.color"
    class="mx-auto"
    max-width="300"
    min-width="300"
    min-height="500"
  >
    <v-img
      :src="data.image"
      height="300px"
      cover
    ></v-img>

    <v-card-title class="title">
      {{data.title}}
    </v-card-title>

    <v-card-subtitle class="poppins">
      {{data.subtitle}}
    </v-card-subtitle>

    <p class="poppins">
      {{data.short}}
    </p>

    <v-card-actions>
      <v-btn
        v-for="action in data.actions" :key="action.name"
        color="orange-lighten-2"
        variant="text"
        :href="action.to" target="_blank"
      >
        {{action.name}}

      </v-btn>

      <v-spacer></v-spacer>

      <v-btn
        :icon="show ? 'mdi-chevron-up' : 'mdi-chevron-down'"
        @click="show = !show"
      ></v-btn>
    </v-card-actions>

    <v-expand-transition>
      <div v-show="show">
        <v-divider></v-divider>

        <v-card-text class="poppins" v-html="data.long">
        </v-card-text>
      </div>
    </v-expand-transition>
  </v-card>
  </v-container>
</template>

<script setup>
  import { ref, onMounted } from 'vue'

defineProps({
  data: Object
})
 const show = ref(false)

</script>
<style scoped>
.title {
  color: white !important;
    font-family: 'Poppins';
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