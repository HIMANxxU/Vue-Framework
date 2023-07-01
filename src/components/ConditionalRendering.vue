<template>
    <h1>Conditional Rendering</h1>
    <h2 v-if="show">If condition</h2>
    <h2 v-else>else Condition</h2>
    <button v-on:click="Toggler()">Toggler</button>
</template>
<script>
export default {
    name: "ConditionalRendering",
    data() {
        return {
            show: true
        }

    }
    ,
    methods: {
        Toggler() {
            this.show = !this.show
        }
    }

}
</script>