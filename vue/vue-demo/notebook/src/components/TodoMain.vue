<template>
    <section>
        <ul>
            <li v-for="(item,index) in list" :key="item.id">
                {{ index+1 }}
                {{ item.name }}
                <button @click="Delete(item.id)">删除</button>
            </li>
        </ul>
    </section>
</template>

<script>
export default {
    props:{ 
        list:Array
    },
    methods:{
        Delete(id){
            this.$emit("Delete",id)
        }
    }
}
</script>

<style>

</style>