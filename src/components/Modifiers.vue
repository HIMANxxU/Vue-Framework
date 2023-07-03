<template>
  <h1>Modifiers in vue</h1>
  <label for="name">Name</label>
  <input
    v-on:change="toggler = false"
    type="text"
    id="name"
    name="name"
    v-model.lazy="name"
  />
  <!-- v-model.trim="name"
    v-model.number="name" -->
  <h2 v-if="toggler">PREVIEW</h2>
  <h2 v-else>{{ name }}</h2>
</template>
<script>
export default {
  name: "ModisierS",
  data() {
    return {
      toggler: true,
      name: null,
    };
  },
};
</script>
