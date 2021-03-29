<template>
  <Capa />
  <main>
    <Sobre />
    <Beneficios/>
    <FaleComigo/>
    <Midias/>
    <Footer/>
  </main>
  <!-- <WhatsApp/> -->
</template>

<script>
import Capa from "./components/Capa";
import Sobre from "./components/Sobre";
import Beneficios from './components/Beneficios';
import FaleComigo from './components/FaleComigo';
import Midias from './components/Midias';
import Footer from './components/Footer';
// import WhatsApp from './components/WhatsApp';

export default {
  name: "App",
  components: {
    Capa,
    Sobre,
    Beneficios,
    FaleComigo,
    Midias,
    Footer
    // WhatsApp
  },
};
</script>

<style>

@import url("https://fonts.googleapis.com/css2?family=Montserrat:wght@100;200;400;500;600;800;900&display=swap");
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}
html {
  font-family: "Montserrat", sans-serif;
  scroll-behavior: smooth;
}
#app {
  position: relative;
  /* font-family: Avenir, Helvetica, Arial, sans-serif;
  -webkit-font-smoothing: antialiased;
  -moz-osx-font-smoothing: grayscale;
  text-align: center;
  color: #2c3e50; */
  /* margin-top: 60px; */
}
</style>
