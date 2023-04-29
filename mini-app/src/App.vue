<template>
  <div id="app">
    <Header />
    <HelloWorld />
    <Todos/>
    <Footer />
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import HelloWorld from "./components/HelloWorld.vue";
import Footer from "./components/Footer.vue";
import Todos from "./components/Todos.vue";

export default {
  name: "App",
  components: {
    Header,
    HelloWorld,
    Todos,
    Footer,
  },
};
</script>

<style>
#app {
  font-family: Arial, Helvetica, sans-serif;
  text-align: center;
}
</style>
