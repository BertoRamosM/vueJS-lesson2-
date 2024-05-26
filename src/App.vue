<template>
 <h1>{{title}}</h1>
 <p>Welcome...</p>
 <div v-if="showModal">
 <Modal  theme="sale" @close="toggleModal">
  <template v-slot:links>
    <a href="">Sign up now</a>
    <a href="">More info</a>
  </template>
  <h1>Ninja giveaway</h1>
  <p>Grab your ninja swag for half price!</p>

</Modal >
 </div>
 <button @click="toggleModal">open modal</button>

 </template>

<script>
import Modal from './components/Modal.vue'

export default {
  name: 'App',

  components: {
    Modal
  },

  data() {
    return {
      title: 'My first vue App', 
      header: "Sign up for the giveaway",
      text: "Grab your ninja swag for half price",
      showModal: false
    }
  },
  methods: {
    toggleModal() {
      this.showModal = !this.showModal
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
.active{
  background: blue;
}
</style>
