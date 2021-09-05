<template>
  <div class="container">
    <Header :date="data.updated.toTimeString()"> </Header>
    <div class="row align-items-center justify-content-center">
      <Box title="Total Cases" :value="data.cases"> </Box>
      <Box title="Today Cases" :value="data.todayCases"> </Box>
    </div>
    <div class="mt-2 row align-items-center justify-content-center">
      <Box title="Total Deaths" :value="data.deaths"> </Box>
      <Box title="Today Deaths" :value="data.todayDeaths"> </Box>
    </div>
    <div class="mt-2 row align-items-center justify-content-center">
      <Box title="Total Recovered" :value="data.recovered"> </Box>
      <Box title="Today Recovered" :value="data.todayRecovered"> </Box>
    </div>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Box from "./components/Box.vue";

export default {
  name: "App",
  components: {
    Header,
    Box,
  },
  data() {
    return {
      data: {},
    };
  },
  async created() {
    const res = await fetch("https://disease.sh/v3/covid-19/all");
    const data = await res.json();
    this.data = data;
    this.data.updated = new Date(this.data.updated);
  },
};
</script>


