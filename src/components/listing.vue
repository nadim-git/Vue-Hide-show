<template>
  <div id="ninja">
    <ul>
      <li
        v-for="student in students"
        v-on:click="student.show = !student.show"
        v-bind:key="student.id"
      >
        <button class="button button1" v-bind:title="message">
          {{ student.name }}
        </button>
        <h3 v-show="student.show">{{ student.speciality }}</h3>
      </li>
    </ul>
  </div>
</template>

<script>
export default {
  props: ["students"],
  data() {
    return {
      message: "click Me To Show",
    };
  },
};
</script>

<style scoped>
header {
  background-color: rgb(168, 201, 201);
  padding: 10px;
}
h1 {
  text-align: center;
}
#ninja {
  width: 100%;
  max-width: 1200px;
  margin: 40px auto;
  padding: 0 20px;
  box-sizing: border-box;
}
ul {
  display: flex;
  flex-wrap: wrap;
  list-style-type: none;
  padding: 0;
}
li {
  flex-grow: 1;
  flex-basis: 300px;
  text-align: center;
  padding: 5px;
  border: 1px solid #222;
  border-radius: 15px;
  margin: 10px;
  background-color: darkgray;
}
.button {
  background-color: #4caf50; /* Green */
  border: none;
  color: white;
  padding: 16px 32px;
  text-align: center;
  text-decoration: none;
  display: inline-block;
  font-size: 16px;
  margin: 4px 2px;
  transition-duration: 0.4s;
  cursor: pointer;
  width: 250px;
  height: 100px;
}

.button1 {
  background-color: white;
  color: black;
  border: 2px solid #4caf50;
  border-radius: 15px;
}
.button1:hover {
  background-color: #4caf50;
  color: white;
}
</style>
