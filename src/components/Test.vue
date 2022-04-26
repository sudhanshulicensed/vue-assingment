<template>
    <div class="form">
        <div class="magic">
            Your Input goes here: {{name}}
        </div>
        <div>
            <label for="naam">Enter Your Name Below</label>
        </div>
        <div>
        <input id="naam" type="text" v-model="name" placeholder="Your Name">
        </div>
        <div class="btn">
            <button v-on:click="removeInput">Clear</button>
            <button v-on:click="upperCase">Caps-ON</button>
        </div>
    </div>
</template>

<script>
export default {
    name: 'TestAgain',
    data() {
        return {
            name: ''
        }
    },
    methods: {
        removeInput(){
            this.name = "";
        },

        upperCase(){
            this.name = this.name.toUpperCase();
        }
    }
}
</script>

<style>

    div{
        display: block;
    }
    .form{
        width: 50%;
        margin-left: auto;
        margin-right: auto;
        height: auto;
        border: 1px solid black;
        font-family: sans-serif;
    }

    input{
        box-sizing: border-box;
        border: none;
        padding: 10px;
        margin-bottom: 10px;
        
    }

    .magic{
        box-sizing: border-box;
        color: #fab1a0;
        margin-bottom: 10px;
    }
</style>