<template>
    <h1>Child comp</h1>
    <button v-on:click="getData(data)"> get data</button>
</template>
<script>
export default {
    name: "ChildProp",
    props: {
        getData: Function,


    },
    data() {
        return {
            data: "This is a msg from child comp",

        }
    }
}
</script>