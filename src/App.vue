<template>
  <div id="app">
    <Navigation></Navigation>
    <PrvaStranica></PrvaStranica>
    <DrugaStranica></DrugaStranica>
  </div>
</template>

<script>
import Navigation from "./components/Navigation";
import PrvaStranica from "./components/PrvaStranica";
import DrugaStranica from "./components/DrugaStranica";

export default {
  name: "app",
  components: {
    Navigation: Navigation,
    PrvaStranica: PrvaStranica,
    DrugaStranica: DrugaStranica,
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
  padding-bottom: 40px;
}
</style>
