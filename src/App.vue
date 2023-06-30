<template>
  <!-- <HelloWorld msg="Welcome to Your Vue.js p" /> -->
  <!-- <ForLoop /> -->
  <!-- <ParentPropS /> -->
  <!-- <ReuMainComp /> -->
  <HtmlBindingVue />
</template>

<script>
// import HelloWorld from "./components/HelloWorld.vue";
// import ForLoop from "./components/ForLoop.vue";
// import ParentPropS from "./components/ParentPropS.vue";
// import ReuMainComp from "./components/ReuMainComp.vue";
import HtmlBindingVue from "./components/HtmlBinding.vue";

export default {
  name: "App",
  components: {
    // HelloWorld,
    // ForLoop,
    // ParentPropS,
    // ReuMainComp,
    HtmlBindingVue,
  },
};
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  width: 100vw;
}
</style>
