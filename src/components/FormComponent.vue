<template>
  <div class="box">
    <!-- our signup form ===================== -->
    <form id="signup-form" @submit.prevent="processForm">
      <!-- name -->
      <div class="field">
        <label class="label">Name</label>
        <input type="text" v-model="name" class="input" name="name" />
      </div>

      <!-- email -->
      <div class="field">
        <label class="label">Email</label>
        <input type="email" class="input" name="email" v-model="email" />
      </div>

      <!-- message -->
      <div class="field">
        <label class="label">Message</label>
        <input type="text" v-model="message" class="input" name="message" />
      </div>

      <!-- buttons -->
      <div class="field is-grouped is-grouped-right">
        <p class="control">
          <button class="button is-danger">Alert</button>
        </p>
        <p class="control">
          <button
            type="submit"
            class="button is-primary"
            @click.prevent="submitted"
          >
            Submit
          </button>
        </p>
      </div>
    </form>
    <br />

    <div class="card" v-if="isSubmitted">
      <header class="card-header">
        <p class="card-header-title is-centered">
          Form Data
        </p>
        <a href="#" class="card-header-icon" aria-label="more options">
          <span class="icon">
            <i class="fas fa-angle-down" aria-hidden="true"></i>
          </span>
        </a>
      </header>
      <div class="card-content">
        <div class="content">
          <p>
            Name: <b>{{ name }}</b>
          </p>
          <p>
            Email: <b>{{ email }}</b>
          </p>
          <p>
            Message: <b>{{ message }}</b>
          </p>
          <a href="#">{{ email }}</a>
          <br />
          <time datetime="2020-1-1">11:09 PM - 1 Jan 2020</time>
        </div>
      </div>
      <footer class="card-footer"></footer>
      <a href="#">@bulmaio</a> | <a href="#">#css</a> |
      <a href="#">#responsive</a>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      message: "",
      name: "",
      email: "",
      isSubmitted: false
    };
  },
  methods: {
    processForm: function() {
      console.log({
        name: this.name,
        email: this.email,
        message: this.message
      });
      alert("Data Processing!");
    },
    submitted() {
      this.isSubmitted = true;
    }
  }
  //props: ["message", "name", "email"]
};
</script>

<style>
.label {
  position: left;
}
</style>
