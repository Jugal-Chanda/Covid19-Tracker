<template>
  <header>
    <h1>Covid19 Tracker</h1>
    <h6>Last Update: {{ date }}</h6>
  </header>
</template>
<script>
export default {
  name: "Header",
  props: {
    date: {
      type: String,
    },
  },
  methods: {},
  data() {
    return {};
  },
};
</script>

<style scoped>
header > h1 {
  text-align: center;
  border-bottom: 2px solid black;
  border-top: 2px solid black;
}
header > h6 {
  text-align: center;
  border-bottom: 2px solid black;
  padding-bottom: 7px;
}
</style>
