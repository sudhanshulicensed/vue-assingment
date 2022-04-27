<template>
    <div class="list">
        <div class="type">
            <p>When you submit data will be added inside of List</p>
            <form v-on:submit.prevent>
            <input v-on:keypress="submit" type="text" v-model="name" placeholder="Type Something over here"/>
        </form>
        <ul>
            <li v-for="(item, index) in data" v-bind:key="index">{{ item }}</li>
        </ul>
        </div>
    </div>
</template>

<script>

export default {
    name: "InFormToList",
    data() {
        return {
            name: "",
            data: [],
        }
    },
    methods: {
        submit (e) {
            // console.log(e)
            if(e.keyCode === 13) {
                this.data.push(this.name);
                this.name = "";
            }
        }
    }    
}
</script>

<style>
    .list{
        width: 40%;
        margin-left: auto;
        margin-right: auto;
    }

    ul{
        width: 50px;
        margin-left: auto;
        margin-right: auto;
    }

    
</style>