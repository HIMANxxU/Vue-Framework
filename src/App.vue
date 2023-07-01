<template>
  <!-- <HelloWorld msg="Welcome to Your Vue.js p" /> -->
  <!-- <Basics /> -->
  <!-- <ConditionalRendering /> -->
  <!-- <InputField /> -->

  <!-- <ForLoop /> -->
  <!-- <ParentPropS /> -->
  <!-- <ReuMainComp /> -->
  <!-- <HtmlBindingVue /> -->
  <!-- <ClassBinding /> -->
  <!-- <ReF /> -->
  <!-- <ParentComp /> -->
  <SimpleFormVue />
</template>

<script>
import SimpleFormVue from './components/Form/SimpleForm.vue';
// import Basics from "./components/Basics.vue";
// import ConditionalRendering from "./components/ConditionalRendering.vue";
// import InputField from "./components/InputField.vue";

// import HelloWorld from "./components/HelloWorld.vue";
// import ForLoop from "./components/ForLoop.vue";
// import ParentPropS from "./components/ParentPropS.vue";
// import ReuMainComp from "./components/ReuMainComp.vue";
// import HtmlBindingVue from "./components/HtmlBinding.vue";
// import ClassBinding from "./components/ClassBinding.vue";
// import ParentComp from "./components/Props/ParentProp.vue"
// import ReF from "./components/Ref.vue";


export default {
  name: "App",
  components: {
    // Basics,
    // ConditionalRendering,
    // InputField,
    // HelloWorld,
    // ForLoop,
    // ParentPropS,
    // ReuMainComp,
    // HtmlBindingVue,
    // ClassBinding,
    // ParentComp,
    // ReF,
    SimpleFormVue
  },
};
</script>

<style>
/* #app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
  width: 100vw;
} */
</style>
