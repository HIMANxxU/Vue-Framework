<template>
  <h1>Watcher in vue</h1>
  <button v-on:click="count = count + 1">+</button>
  <button v-on:click="count = count - 1">-</button>
  <h1>{{ count }}</h1>
</template>
<script>
export default {
  name: "WatcherS",
  data() {
    return {
      count: null,
    };
  },

  watch: {
    count(newcount, prevCount) {
      if (newcount > 5 && newcount > prevCount) {
        alert("stop");
      }
    },
  },
};
</script>
