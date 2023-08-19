<template>
    <header class="header">
        <h1>小黑记事本</h1>
        <input placeholder="请输入任务" v-model="TodoName" @keyup.enter="submit">
        <button @click="submit">提交</button>
    </header>
</template>

<script>
export default {
    data() {
        return{
            TodoName:''
        }
     },
     methods: {
        submit() {
            if (this.TodoName === '') {
                alert('任务名不能为空')
            }
            else{
                this.$emit('submit',this.TodoName)
                this.TodoName=''
            }

        }
      }
}
</script>

<style>

</style>