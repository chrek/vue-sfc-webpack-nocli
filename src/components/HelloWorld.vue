<template>
  <div class="hello">
    <h1>{{ message }}</h1>
  </div>
</template>

<script>
export default {
  name: "HelloWorld",
  props: {
    message: String
  }
};
</script>

<!-- Add "scoped" attribute to limit CSS to this component only -->
<style scoped>
h1 {
  margin: 20px 0 20px;
  font-size: 24px;
  font-family: "Roboto", sans-serif;
  text-align: center;
}
</style>
