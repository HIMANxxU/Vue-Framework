<template>
  <div class="card">
    <h3>Name : {{ data.name }}</h3>
    <h3>Email : {{ data.email }}</h3>
    <h3>Profession : {{ gg }}</h3>
  </div>
  <button v-on:click="getName(`Name is :  ${data.name}`)">Get name</button>
</template>
<script>
export default {
  name: "ReusableComp",
  props: {
    data: Object,
    getName: Function,
    gg: String,
  },
};
</script>
<style>
.card {
  /* width: 200px; */
  border: 2px solid black;
  border-radius: 5px;
  padding: 10px;
}
</style>
