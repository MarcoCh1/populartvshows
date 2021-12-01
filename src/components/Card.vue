<template>
  <div class="card" style="width: 18rem">
    <img v-bind:src="image" class="card-img-top" alt="..." />
    <div class="card-body">
      <h5 class="card-title">{{ title }}</h5>
      <p class="card-text">{{ overview }}</p>
      <!-- <a href="#" class="btn btn-primary">Go somewhere</a> -->
    </div>
  </div>
</template>



<script>
// import App from "App.vue";

export default {
  name: "Card",
  props: ["title", "overview", "image"],
};
</script>

<style scoped>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

.card {
  text-align: center;
  padding: 10px;
  margin: 0px;
  display: inline-flex;
  margin-top: 30px;
}

.card[data-v-54cdc180] {
  text-align: center;
  padding: 10px;
  margin: 0px;
  display: inline-flex;
  margin-top: 30px;
  margin-left: 20px;
}

/* .card[data-v-54cdc180] {
  text-align: center;
  padding: 10px;
  margin: 0px;
  display: inline-flex;
  margin-left: 60px;
} */
</style>
