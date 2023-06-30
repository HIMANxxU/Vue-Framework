<template>
  <h1>For loop in vue</h1>
  <h2 v-for="details in user" :key="details">
    Name is :{{ details.name }} and Email is :{{ details.email }}
  </h2>
</template>
<script>
export default {
  name: "ForLoop",
  data() {
    return {
      user: [
        {
          name: "John Dow",
          email: "john.doe@example.com",
        },
        {
          name: "Jane Smith",
          email: "jane.smith@example.com",
        },
        {
          name: "Michael Johnson",
          email: "michael.johnson@example.com",
        },
        {
          name: "Emily Brown",
          email: "emily.brown@example.com",
        },
        {
          name: "David Davis",
          email: "david.davis@example.com",
        },
        {
          name: "Sarah Wilson",
          email: "sarah.wilson@example.com",
        },
        {
          name: "Robert Anderson",
          email: "robert.anderson@example.com",
        },
        {
          name: "Olivia Martinez",
          email: "olivia.martinez@example.com",
        },
        {
          name: "William Thompson",
          email: "william.thompson@example.com",
        },
        {
          name: "Sophia Taylor",
          email: "sophia.taylor@example.com",
        },
      ],
    };
  },
};
</script>
<style scoped>
h2:nth-child(even) {
  color: rgb(35, 35, 113);
}
</style>
