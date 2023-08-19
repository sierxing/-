<template>
    <div id="app">
        <TodoHeader @submit="submit"></TodoHeader>
        <TodoMain :list="list" @Delete="Delete"></TodoMain>
        <TodoFooter :list="list" @clearup="clearup"></TodoFooter>
    </div>
</template>

<script>
import Temp from './components/Temp.vue';
import TodoHeader from './components/TodoHeader.vue';
import TodoMain from './components/TodoMain.vue';
import TodoFooter from './components/TodoFooter.vue';
export default {
    components: { 
        Temp,
        TodoHeader,
        TodoMain,
        TodoFooter
    },
    data(){
        return{
            list: [
                {id:1,name:'吃饭'},
                {id:2,name:'睡觉'},
                {id:3,name:'打豆豆'}
            ]
        }
    },
    methods: {
        submit(TodoName) {
            this.list.push({
                id:this.list.length+1,
                name:TodoName
            })
         },
         Delete(id){
            this.list = this.list.filter((list)=>list.id!==id)
         },
         clearup(){
            this.list=[]
         }
    }
}
</script>

<style>

</style>