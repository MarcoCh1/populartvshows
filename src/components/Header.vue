<template>
  <div class="header">
    <h1 id="titleText">{{ theTitle }}</h1>
  </div>
</template>

<script>
export default {
  name: "Header",
  props: ["theTitle"],
};
</script>

<style scoped>
.header {
  background: rgb(0, 0, 0);
  color: white;
  text-align: center;
  padding: 10px;
  margin: 0px;
}

#titleText {
  font-family: "Franklin Gothic Medium", "Arial Narrow", Arial, sans-serif;
}
</style>