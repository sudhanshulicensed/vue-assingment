<template>
    <div class="outer-div">
        {{name}}
    </div>
</template>

<script>

export default {
    name: 'ConsoleLogs',
    data () {
        return{
            name: "Sky"
    };
    },
    created: function() {
        console.log("Console Log: Created");
    },

    mounted: function() {
        console.log("Console Log: Mounted");
    },

    updated: function(){
        console.log("Console Log: Updated eys");
    },

    destroyed: function(){
        console.log("Console Log: Destroyed");
    },
    // methods:{
    //     upperCase(){

    //     }
    // }
}
</script>
