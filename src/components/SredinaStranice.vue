<template>
  <div id="app2" class="container">
    <div>
      <h1>My Profil</h1>
      <PrvaStranica></PrvaStranica>
      <DrugaStranica></DrugaStranica>
    </div>
  </div>
</template>

<script>
import PrvaStranica from "./components/PrvaStranica";
import DrugaStranica from "./components/DrugaStranica";

export default {
  name: "app2",
  components: {
    PrvaStranica: PrvaStranica,
    DrugaStranica: DrugaStranica,
  },
};
</script>

<style>
.container {
  width: 70%;
  margin: 0 auto;
  padding-bottom: 40px;
}
.container h1 {
  font-weight: bold;
  font-size: 45px;
  line-height: 25px;
  margin: 60px 0;
}
</style>