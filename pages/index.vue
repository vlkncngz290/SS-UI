<template>
  <div class="container">
    <button v-on:click="test">TEST</button>
  </div>
</template>

<script>
export default {
  name: 'IndexPage',
  methods:{
    async test(){
      console.log(this.$axios.defaults)
      //let test=await this.$axios.post('prediction',{})
      //console.log("predictions",test)
    }
  }
}
</script>
