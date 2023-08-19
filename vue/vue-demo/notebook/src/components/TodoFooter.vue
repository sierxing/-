<template>
  <div>
    <p>合计：{{ list.length }}</p>
    <button @click="clearup">清空</button>
  </div>
</template>

<script>
export default {
    props:{
        list:Array
     },
     methods:{
        clearup(){
            this.$emit('clearup')
        }
     }
}
</script>

<style>

</style>