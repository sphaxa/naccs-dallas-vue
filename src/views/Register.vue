<template>
  <div class="register">
    <Navigation />
  <div><p></p></div>
    <Form />
  </div>
</template>

<script>
// @ is an alias to /src
import Form from "@/components/Form.vue";
import Navigation from "@/components/Navigation.vue";

export default {
  name: "Register",
  components: {
    Form,
    Navigation
  }
};
</script>
