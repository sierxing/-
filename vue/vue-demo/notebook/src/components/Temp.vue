<template>
  <div class="progress">
    <button @click="count--">-</button>
    {{ count }}
    <button @click="count++">+</button>
  </div>
</template>

<script>
export default {
  props:{
    count:{
      type:Number
    }
  }
}
</script>

<style>

</style>