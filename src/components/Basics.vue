<template>
    <h1>Basics of vue</h1>
    <h2>Hello from Demo {{ msg }}</h2>
    <h2>My age is {{ Age }}</h2>
    <h2>Work status: {{ getStatus() }}</h2>
    <h2>Get Name: {{ getName() }}</h2>
    <h2>Get Details: {{ getDetails() }}</h2>
    <h2>Get Phone from details: {{ getDetails().phone }}</h2>
    <h2 v-on:mouseover="handelMouseHover()">
        Get Age from details using .this: {{ getDetails().Age }}
    </h2>
    <button v-on:click="Alert(btn)">{{ (btn = "button1") }}</button>
    <h2>Count Value{{ count }}</h2>
    <button v-on:click="CountIncr()">+</button>
    <br>
    <input type="text" v-model="inputData">
    <h2>{{ inputData }}</h2>

    <hr>
</template>
<script>
export default {
    name: "BasicS",
    props: {
        msg: String,
    },
    data() {
        return {
            Age: "23",
            count: 0,
            inputData: "",

            getStatus: function () {
                return "working...";
            },
        };
    },
    methods: {
        getName() {
            return "himanshu";
        },
        getDetails() {
            return {
                phone: 1234,
                email: "himanshu@gmail.com",
                Age: this.Age,
            };
        },
        Alert(btn) {
            alert(`${btn} Called`);
        },
        handelMouseHover() {
            console.log("Mouse Hover Trigred");
        },
        CountIncr() {
            this.count = this.count + 1;
        },
    },
};
</script>
<style>
button {
    display: block;
    margin: auto;
}
</style>
