<template>
  <div id="app">
    <Navigation></Navigation>
    <SredinaStranice>
      <PrvaStranica></PrvaStranica>
      <DrugaStranica></DrugaStranica>
    </SredinaStranice>
  </div>
</template>

<script>
import Navigation from "./components/Navigation";
import SredinaStranice from "./components/SredinaStranice";
import PrvaStranica from "./components/PrvaStranica";
import DrugaStranica from "./components/DrugaStranica";

export default {
  name: "app",
  components: {
    Navigation: Navigation,
    SredinaStranice: SredinaStranice,
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
</style>
