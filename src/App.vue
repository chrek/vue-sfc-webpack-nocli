<template>
  <div id="app" class="hero is-fullheight is-success is-bold">
    <div class="hero-body">
      <div class="container">
        <h1 class="title has-text-centered">
          Form Processing in Vue.js
        </h1>
        <!-- <HelloWorld :msg="message"/> -->
        <!-- <h3 class="title has-text-centered">
          {{message}}
        </h3> -->
        <HelloWorld message="Hello World" />
        <HelloWorld :message="message" />
        <!-- <form-component :message="message"></form-component> -->
        <form-component></form-component>
      </div>
    </div>
  </div>
</template>

<script>
import HelloWorld from "./components/HelloWorld.vue";
import FormComponent from "./components/FormComponent.vue";
export default {
  data() {
    return {
      message: "Hello Vue",
      name: "",
      email: ""
    };
  },
  methods: {
    alertMessage() {
      alert(this.message);
    }
  },
  components: {
    HelloWorld,
    "form-component": FormComponent
  }
};
</script>

<style>
#app {
  /* text-align: center; */
  font-size: 18px;
  font-family: "Roboto", sans-serif;
  /* color: blue; */
  margin-top: 50px;
}

.message {
  font-size: 18px;
  font-family: "Roboto", sans-serif;
  /* color: blue; */
}
</style>
