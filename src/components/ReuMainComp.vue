<template>
  <div class="reusable-comp">
    <div v-for="user in users" :key="user.name">
      <ReusableComp :data="user" :getName="getName" :gg="profession" />
    </div>
  </div>
</template>
<script>
import ReusableComp from "./ReusableComp.vue";
export default {
  name: "ReuMainComp",
  components: {
    ReusableComp,
  },
  data() {
    return {
      users: [
        { name: "Aarav Kumar", email: "aarav.kumar@example.com" },
        { name: "Aanya Sharma", email: "aanya.sharma@example.com" },
        { name: "Advait Patel", email: "advait.patel@example.com" },
        { name: "Anaya Desai", email: "anaya.desai@example.com" },
        { name: "Arjun Gupta", email: "arjun.gupta@example.com" },
        { name: "Avni Shah", email: "avni.shah@example.com" },
        { name: "Devika Joshi", email: "devika.joshi@example.com" },
      ],
      profession: "Engineers",
    };
  },
  methods: {
    getName(any) {
      alert(any);
    },
  },
};
</script>
<style>
.reusable-comp {
  display: flex;
  column-gap: 20px;
  row-gap: 20px;
  flex-wrap: wrap;
}
</style>
