<template>
  <div id="app">
    <div class="container-fluid">
      <TheHeader />

      <main class="position-relative">
        <TheBanner />
      </main>

      <TheFooter />
    </div>
  </div>
</template>

<script>
import TheHeader from "./components/TheHeader.vue";
import TheBanner from "./components/TheBanner.vue";
import TheFooter from "./components/TheFooter.vue";

export default {
  name: "App",
  components: { TheHeader, TheBanner, TheFooter },
};
</script>

<style lang="scss">
@import "./assets/sass/style.scss";
#app {
  background-color: #f6f7f1;
}
</style>
