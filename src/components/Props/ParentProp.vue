<template>
    <h1>Parent prop {{ Actualmsg }}</h1>


    <ChildProp :getData="getChildData" />
</template>
<script>
import ChildProp from "./ChildProp.vue"
export default {
    name: "ParentComp",
    components: {
        ChildProp
    },
    data() {
        return {
            Actualmsg: null,

        }
    },
    methods: {
        getChildData(msg) {

            this.Actualmsg = msg




        }
    }
}
</script>