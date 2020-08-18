<template>
  <div id="app">
    <Navigation></Navigation>
    <SredinaStranice></SredinaStranice>
  </div>
</template>

<script>
import Navigation from "./components/Navigation";
import SredinaStranice from "./components/SredinaStranice";

export default {
  name: "app",
  components: {
    Navigation: Navigation,
    SredinaStranice: SredinaStranice,
  },
};
</script>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
  font-family: Arial;
  font-style: normal;
}

.container {
  width: 70%;
  margin: 0 auto;
}
</style>
