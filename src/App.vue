<template>
 <h1>{{title}}</h1>
 <input type="text" ref="name">
 <button @click="handleClick">Click event</button>
</template>

<script>
export default {
  name: 'App',
  data() {
    return {
      title: 'My first vue App'
    }
  },
  methods: {
    handleClick() {
      console.log(this.$refs.name)
    }
  }
}
</script>


//query selector in js in vue template refs
<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
h1{
  border-bottom: 1px solid #ddd;
  display: inline-block;
  padding-bottom: 10px;
}
</style>
