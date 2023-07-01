<template>
    <h1>Ref in vue JS</h1>
    <input type="text" ref="myref">
    <button v-on:click="getRefValue"> button</button>
    <h1>{{ accessRef }}</h1>
</template>
<script>
export default {
    name: "ReF",
    data() {
        return {
            accessRef: null

        }
    },
    methods: {
        getRefValue() {
            this.$refs.myref.style.backgroundColor = "red"
            this.accessRef = this.$refs.myref.value


            console.log("hello")
        }

    }
}
</script>