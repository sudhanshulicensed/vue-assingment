<template>
    <div>
        Using Array over dropdown
        <div v-bind:style="{color: color_value.color}">This will be changing</div>
        <select v-model="color_value">
            <option v-for="(col, index) in colors" v-bind:key="index" v-bind:value="{color: col}">
                {{col}}
            </option>
        </select>
    </div>
</template>

<script>
export default {
    name: "ArrDropDown",
    data(){
        return {
            colors: ["red", "blue", "green", "purple"],
            color_value: {
                color: "black",
            }
        }
    },

}
</script>