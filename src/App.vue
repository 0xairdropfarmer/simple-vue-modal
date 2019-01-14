<template>
  <div id="app">
    <img width="25%" src="./assets/logo.png" />
    <h1>Hello, I'm a Vue Project</h1>
    <button class="btn" @click="showModal">Click me!</button>
    <Modal v-show="isModalVisible" @close="closeModal" />
  </div>
</template>

<script>
import Modal from "./components/Modal.vue";

export default {
  name: "App",
  components: {
    Modal
  },
  data() {
    return {
      isModalVisible: false
    };
  },
  methods: {
    showModal() {
      this.isModalVisible = true;
    },
    closeModal() {
      this.isModalVisible = false;
    }
  }
};
</script>

<style>
#app {
  font-family: "Avenir", Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50;
  margin-top: 60px;
}
.btn {
  color: white;
  background: #000;
  border: 1px solid #828282;
  border-radius: 2px;
  margin: 4px;
  padding: 5px;
}
</style>
