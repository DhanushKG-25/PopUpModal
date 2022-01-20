<template>
<h1>{{title}}</h1>
<Modal v-if="showModal"  theme="sale" @close="handleShowModal">
  <template v-slot:links>
    <a href="#">Sign up</a>
    <a href="#">More Info</a>
  </template>
  <h1>Sign up for the Ninja giveaway</h1>
  <p>Grab your ninja swag for half price</p>
</Modal>
<Modal v-if="showModalTwo"  theme="" @close="handleShowModalTwo">
  <template v-slot:links>
    <a href="#">Sign up</a>
    <a href="#">More Info</a>
  </template>
  <h1>Sign up for the Dhanush giveaway</h1>
  <p>Grab your Dhanush swag for half price</p>
</Modal>
<button @click="handleShowModal">Open Popup1</button>
<button @click="handleShowModalTwo">Open Popup2</button>
</template>

<script>
import Modal from '../src/components/Modal.vue'

export default {
  name: 'App',
  data(){
    return {
      title: 'My First Vue Project',
      heading: 'Sign up for the giveaway',
      text:'Grab your ninja swag for half price',
      showModal: false,
      showModalTwo: false
    }
  },
  components:{
    Modal
  },
  methods:{
    handleShowModal(){
      this.showModal = !this.showModal
    },
    handleShowModalTwo(){
      this.showModalTwo = !this.showModalTwo
    }
  }
}
</script>

<style>
#app {
  font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
button {
  background: #bbb;
  padding: 10px;
  border: none;
  border-radius: 4px;
  margin: 10px;
  font-size: 16px;
  color: #333;
}
</style>
