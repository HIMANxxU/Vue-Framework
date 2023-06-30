<template>
  <h1>Child Comp for Props</h1>
  <h2>Incoming DATA :{{ userslist }}</h2>
  <h2>Incoming props msg : {{ msg }}</h2>
  <button v-on:click="getdata()">button</button>
</template>
<script>
export default {
  name: "ChildPropS",
  props: {
    msg: String,
    userslist: Array,
    getdata: Function,
  },
};
</script>
