<template>
  <h1>{{ title }}</h1>
  <p>Welcome...</p>


  <teleport to=".modals" v-if="showModal">
    <Modal theme="" @close="toggleModal">
      <template v-slot:links>
        <a href="">Sign up now</a>
        <a href="">More info</a>
      </template>
      <h1>Ninja giveaway</h1>
      <p>Grab your ninja swag for half price!</p>
    </Modal>
  </teleport>

  <teleport to=".modals" v-if="showModal2">
    <Modal @close="toggleModal2">
      <h1>Sign up to the newslatter</h1>
      <p>For updates and promo codes!</p>
    </Modal>
  </teleport>

  <button @click="toggleModal">open modal</button>
  <button @click="toggleModal2">open modal 2</button>
</template>

<script>
import Modal from "./components/Modal.vue";

export default {
  name: "App",

  components: {
    Modal,
  },

  data() {
    return {
      title: "My first vue App",
      showModal: false,
      showModal2: false,
    };
  },
  methods: {
    toggleModal() {
      this.showModal = !this.showModal;
    },
    toggleModal2() {
      this.showModal2 = !this.showModal2;
    },
  },
};
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
h1 {
  border-bottom: 1px solid #ddd;
  display: inline-block;
  padding-bottom: 10px;
}
.active {
  background: blue;
}
</style>
