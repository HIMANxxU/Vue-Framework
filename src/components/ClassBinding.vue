<template>
    <h1>Class binding in vue</h1>
    <h3 :class="{ green: colorfull, err: errorStatus }">Hello World</h3>
    <h3 :class="getClasses">Hello World</h3>

    <button v-on:click="colorfull = !colorfull"> Button toggler</button>
    <button v-on:click="errorStatus = !errorStatus"> error toggler</button>
</template>
<script>
export default {
    name: "ClassBinding",
    data() {
        return {
            colorfull: true,
            errorStatus: false

        }
    },
    computed: {
        getClasses() {
            return { class1: true, class2: true, class3: true }

        }


    }

}
</script>
<style>
.green {
    background-color: rgb(29, 166, 29);
    width: 300px;
    text-align: center;
    padding: 10px;
}

.err {
    color: rgb(250, 222, 215);
    background: red;
}

.class1 {
    padding: 10px;
}

.class2 {
    border: 1px solid black;
    border-radius: 10px;
}

.class3 {
    color: aqua
}
</style>