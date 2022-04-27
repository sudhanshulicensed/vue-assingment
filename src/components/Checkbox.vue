<template>
    <div class="colorRed">
    <div :class="{red: isRed}">
                {{name}}
        </div>
        <input type="checkbox" v-model="isRed" @click="red" :checked="isRed">
    </div>
</template>

<script>
export default {
    name: "CheckBox",
    data() {
        return {
            name: "Sky",
            isRed: false,
        }
    },
    methods: {
        red: function(){
            this.isRed = true;
            console.log(this.isRed)
        }
    }   
}
</script>

<style>
    .red{
        color: red;
    }
</style>