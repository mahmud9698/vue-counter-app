<template>
  <main>
    <div>
      <h4>The current count is ...</h4>
      <h1>{{ count }}</h1>
      <button @click="clickSubtract">-</button>
      <button @click="clickAdd">+</button>
    </div>
  </main>
</template>

//using options API, uncomment to use
<!-- <script>
export default {
  data (){
    return {
      count: 0
    }
  },
  methods:{
    clickAdd (){
      this.count = this.count + 1
    },
    clickSubtract (){
      this.count = this.count -1
    }
  } 
}
</script> -->

//using composition API, uncomment to use
<script setup>
  import {ref} from "vue"
  const count = ref(0)

  const clickAdd = () => {
    count.value = count.value + 1
  }
  
  const clickSubtract = () => {
    count.value = count.value - 1
  }
</script>

<style scoped>
main{
  height: 100vh;
  width: 100vw;
  display: flex;
  justify-content: center;
  align-items: center;
}

div{
  text-align: center;
}
</style>