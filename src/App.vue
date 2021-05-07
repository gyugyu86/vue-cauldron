<template>
  <div id="app">
    <Header></Header>
    <Input></Input>
    <Footer></Footer>
  </div>
</template>

<script>
import Header from "./components/Header.vue";
import Input from "./components/Input";
import Footer from "./components/Footer";

export default {
  components: {
    Header: Header,
    Input: Input,
    Footer: Footer,
  },
};
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
</style>
