<script setup>
import Header from "../components/Header.vue";
import Card from "../components/Card.vue"; 
import datas from '../data/db.json';             
// import axios from "axios";
import { ref } from "vue";

// Mode Import json direct
const data = ref(datas);
const error = ref(null);

// Mode Axios
// const dataFetch = onMounted(async () => {
//   try {
//     const response = await axios.get("http://localhost:3000/lodging");
//     data.value = response.data;
//   } catch (err) {
//     error.value = err;
//   }
// });

// Mode Fetch
// fetch("http://localhost:3000/lodging")
//   .then((res) => res.json())
//   .then((json) => (data.value = json))
//   .catch((err) => (error.value = err));
</script>

<template>
  <div class="home">
    <Header titreHeader="Kasa" />
    <div v-if="error">Oops! Error encountered: {{ error.message }}</div>
    <div class="cards" v-else-if="data">
      <Card v-bind:lodging="data.lodging" />
    </div>
    <div v-else>Loading...</div>
  </div>
</template>

<style lang="scss" scoped>
.home {
  width: 100%;
  @media screen and (min-width: 768px) {
    max-width: 1240px;
    width: 100%;

  }
  .cards {
    display: flex;
    padding: 20px;
    flex-wrap: wrap;
    gap: 60px;
    justify-content: center;
    @media screen and (min-width: 768px) {
     background-color: aliceblue;
     border-radius: 10px;
     padding: 40px 0;

    }
  }
}
</style>
