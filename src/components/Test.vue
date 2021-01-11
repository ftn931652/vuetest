<template>
  <div class="test">
    <input type="text" v-model="text" @keyup.enter="addtask">
    <button v-on:click="addtask">Submit</button>
    <p v-for="(task,index) in todo_list" v-bind:key="index+'aaaaa'" >
        {{task}}
    </p>
  </div>

</template>

<script>
export default {
name:"Test",
data(){
    return{
        todo_list:[],
        text:"",
    }
},
methods:{
   addtask(){
       this.todo_list.push(this.text)
       this.text=""
   }
}
}
</script>

<style>

</style>