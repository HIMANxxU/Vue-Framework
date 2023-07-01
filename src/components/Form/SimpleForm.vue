<template>
    <h1>This is a simple form in vue js</h1>
    <form @submit.prevent="getFormData">
        <label for="name">Name</label>
        <input type="text" name="name" id="name" v-model="daa.name">
        <br><br><br>
        <label for="email">Email</label>
        <input type="text" name="email" id="email" v-model="daa.email">
        <br><br><br>
        <label for="Age">Age</label>
        <input type="text" name="Age" id="Age" v-model="daa.Age">
        <br><br><br>
        <button> Submit</button>


    </form>
    <h1>{{ daa }}</h1>
</template>

<script>

export default {

    name: "SimpleForm",
    data() {
        return {
            Array: [],
            daa: {
                name: null,
                email: null,
                Age: null,
            }

        }
    },
    methods: {
        getFormData() {
            console.log(this.daa)
        }
    }

}

</script>