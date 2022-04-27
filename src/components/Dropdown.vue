<template>
        <div class="drop" v-bind:style="{color: color_value.color}">
        {{ name }} <br>
            <select v-model="color_value">
                <option v-bind:value="{color: 'red'}">Red</option>
                <option v-bind:value="{color: 'blue'}">Blue</option>
                <option v-bind:value="{color: 'green'}">Green</option>
                <option v-bind:value="{color: 'purple'}">Purple</option>
            </select>
        </div>
</template>

<script>
export default {
    name: "DropDown",
    data() {
        return {
            name: "Sky is changing colors",
            color_value: {
                color: "black"
            }
        }
    },
}
</script>

<style>
    /* .dropdown{
        margin: 10px;
        border: 1px solid black;
        width: 60%;
        margin-left: auto;
        margin-right: auto;
    } */

    .drop{
        margin: 10px;
        width: 40%;
        margin-left: auto;
        margin-right: auto;
    }

</style>