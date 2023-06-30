<template>
  <h1>Parent Comp for Props</h1>
  <ChildPropS msg="hello" :userslist="users" :getdata="getdata" />
</template>
<script>
import ChildPropS from "./ChildPropS.vue";
export default {
  name: "ParentProp",
  components: {
    ChildPropS,
  },
  data() {
    return {
      users: ["himanshu", "vishal", "pankaj"],
    };
  },
  methods: {
    getdata() {
      console.log(this.users.push("na"));
    },
  },
};
</script>
