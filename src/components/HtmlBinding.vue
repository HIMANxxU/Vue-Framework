<template>
  <p>HTML BINDING</p>
  <div v-html="tag"></div>
</template>
<script>
export default {
  data() {
    return {
      text: "himanshu",
      tag: "<h1>himanshu</h1>",
    };
  },
};
</script>
