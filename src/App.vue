<template>
  <div class="app">
    <Header/>
    <div class="row">
      <ServerStatus/>
      <ServerDetails/>
    </div>
    <hr>
    <Footer/>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import ServerStatus from "./components/ServerStatus";
import ServerDetails from "./components/ServerDetails";
import Footer from "./components/Footer.vue";

export default {
  name: "app",
  components: {
    Header,
    ServerStatus,
    ServerDetails,
    Footer
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
</style>
