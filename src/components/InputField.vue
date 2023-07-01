<template>
    <h1>Getting data from inpur field</h1>
    <label for="email">
        <h3>Email</h3>
    </label>
    <input type="text" id="email" v-model="email">
    <br>
    <label for="pass">
        <h3>Pass word</h3>
    </label>
    <input type="text" id="pass" v-model="pass">
    <br><br>
    <label for="Vue">Vue</label>
    <input type="checkbox" id="Vue" value="Vue" v-model="technology">
    <br>
    <label for="React">React</label>
    <input type="checkbox" id="React" value="React" v-model="technology">
    <br>
    <label for="Angular">Angular</label>
    <input type="checkbox" id="Angular" value="Angular" v-model="technology">
    <br>
    <label for="student">student</label>
    <input type="radio" value="student" id="student" name="proff" v-model="profession">

    <label for="devloper">devloper</label>
    <input type="radio" value="devloper" id="devloper" name="proff" v-model="profession">
    <h2> {{ email }}</h2>
    <h2>{{ pass }}</h2>
    <h2>{{ profession }}</h2>
    <h2>{{ technology }}</h2>
    <button v-on:click="getValues()">Button</button>
</template>
<script>
export default {
    name: "InputField",
    data() {
        return {
            email: null,
            pass: null,
            technology: [],
            profession: null


        }
    }
    , methods: {
        getValues() {
            console.log(`Values: Email:${this.email}, Pass:${this.pass} ,Technology Stack:${this.technology}`)
        }


    }
}
</script>