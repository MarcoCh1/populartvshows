<template>
  <div id="app">
    <Header theTitle="Popular TV Shows"></Header>
    <Card
      v-for="task in tasks.slice(0, 4)"
      v-bind:key="task.id"
      v-bind:title="task.name"
      v-bind:overview="task.overview"
      v-bind:image="imageUrl + task.poster_path"
      >Tet</Card
    >
  </div>
</template>

<script>
import axios from "axios";
import Header from "./components/Header.vue";
import Card from "./components/Card.vue";
import "bootstrap";
import "bootstrap/dist/css/bootstrap.min.css";

export default {
  name: "App",
  components: {
    Header,
    Card,
  },

  data() {
    return {
      tasks: "",
      imageUrl: "https://image.tmdb.org/t/p/w342",
    };
  },

  methods: {
    getApiArray(response) {
      this.arryItems = response;
    },
  },
  mounted() {
    axios
      .get(
        "https://api.themoviedb.org/3/tv/popular?api_key=1b62ccff88d2cd537027e1d82920197b&language=en-US&page=1"
      )
      .then((response) => {
        let shows = response.data.results;

        // Then sets it to the public array variable using .this
        this.tasks = shows;
      });
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 0px;
}

* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  background: url("https://wallpaperboat.com/wp-content/uploads/2019/11/cinema-05.jpg");
}
</style>
