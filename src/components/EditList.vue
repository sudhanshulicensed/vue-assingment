<template>
    <div class="listedit">
        <p>The list items can be edited and Deleted.</p>
        <p>Enter what you want to enter down below</p>
        <form v-on:submit.prevent>
            <input v-model="name" v-on:keypress="submit" type="text" placeholder="" class="edit-list">
        </form>
        <ol>
            <li class="in-li" v-for="(item, index) in data" v-bind:key="index">{{item}}
            <div class="in-div">
                <a href="#" v-on:click.prevent="editItem(index) ">Edit</a>
                <a href="#" v-on:click.prevent="deleteItem(index)" >Delete</a>
            </div>
            </li>
        </ol>
    </div>
</template>

<script>

import Vue from "vue"

export default {
    name: 'EditList',
    data(){
        return {
            name: "",
            data: [],
            editIndex: false,
        }
    },
    methods: {
        submit(e) {
            if(e.keyCode === 13) {
                if(this.editIndex) {
                    Vue.set(this.editIndex, this.name, this.data);
                    this.name = "";
                    this.editIndex = -1;
                } else {
                    this.data.push(this.name);
                    this.name = "";
                }
            }
        },
        deleteItem(index) {
            this.data.splice(index, 1);
        },
        editItem(index){
            this.editIndex = index;
            this.name = this.data[index];
        }   

        

    }
}
</script>

<style>
    .listedit{
        width: 50%;
        margin: 10px auto;
        border: 1px solid black;
    }

    .edit-list{
        border: 1px solid yellowgreen;
    }

    .in-li{
        display: inline-block;
        box-sizing: border-box;
        width: 60%;
        margin-left: auto;
        margin-right: auto;
        box-sizing: border-box;
        padding: 10px;
        border: 1px solid springgreen;
    }

    .in-div{
        display: inline-block;
        padding-left: 10px;
    }

    .in-div a{
        padding-left: 3px;
    }
</style>