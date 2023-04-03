<script setup>
import Home from "./views/Home.vue";
import { ref } from "vue";
let titre = ref("Kasa");
</script>

<template>
  <div class="container">
    <Home v-bind:title="titre" />
  </div>
</template>

<style lang="scss">

*{
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: Arial, Helvetica, sans-serif;
}

.container {
  width: 100%;
  margin: 0 auto;
  @media screen and (min-width: 768px) {
    max-width: 1400px; 
    padding: 0 100px;   
  }
    
  }

</style>
