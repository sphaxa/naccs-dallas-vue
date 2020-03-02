<template>
  <div class="home">
    <Navigation />
  <div><p></p></div>
    <Splash />
  </div>
</template>

<script>
// @ is an alias to /src
import Splash from "@/components/Splash.vue";
import Navigation from "@/components/Navigation.vue";

export default {
  name: "Home",
  components: {
    Splash,
    Navigation
  }
};
</script>
