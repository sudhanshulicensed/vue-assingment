<template>
    <div>
        {{name}} : {{time}}
    </div>
</template>

<script>
export default {
    name: "TimeCheck",
    data () {
        return{
            name: "Component was created on:",
            time: ""
        }
    },
    created: function() {
        console.log("Console Log: Created");
        this.time = new Date();
    },

    mounted: function() {
        console.log("Console Log: Mounted");
        this.time = new Date();
    },

    updated: function(){
        console.log("Console Log: Updated eys");
        // this.time = new Date();
    },

    destroyed: function(){
        console.log("Console Log: Destroyed");
        this.time = new Date();
    },
}
</script>