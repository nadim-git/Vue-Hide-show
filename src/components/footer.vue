<template>
  <header>
    <h1>{{ Copyright }}</h1>
  </header>
</template>

<script>
export default {
  name: "Footer",
  data() {
    return {
      Copyright: "Copyright 2018-2021 | Nadim Rajpura",
    };
  },
};
</script>

<style scoped>
header {
  background-color: rgb(86, 90, 48);
  padding: 6px;
}
h1 {
  text-align: center;
  font-size: 25px;
  font-family: "Lucida Sans", "Lucida Sans Regular", "Lucida Grande",
    "Lucida Sans Unicode", Geneva, Verdana, sans-serif;
  color: black;
}
</style>
