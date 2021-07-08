<template>
  <div id="app">
    <Header></Header>
    <Listing v-bind:students="students"></Listing>
    <Footer></Footer>
  </div>
</template>

<script>
import Header from "./components/header.vue";
import Listing from "./components/listing.vue";
import Footer from "./components/footer.vue";

export default {
  components: {
    Header,
    Footer,
    Listing,
  },
  name: "App",
  data() {
    return {
      students: [
        { name: "Nadim", speciality: "Web Developer", show: false },
        { name: "vasim", speciality: "HTML Wizardry", show: false },
        { name: "shakil", speciality: "Click Events", show: false },
        { name: "mohammad", speciality: "Conditionals", show: false },
        { name: "mustakim", speciality: "Webpack", show: false },
      ],
    };
  },
};
</script>

<style scoped>
</style>
