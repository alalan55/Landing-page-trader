<template>
  <header>
    <nav>
      <input type="checkbox" id="check" v-on:click="abreNavbar()" />
      <label for="check" class="checkbtn">
        <i class="fas fa-bars"></i>
      </label>
      <div class="logo">LOGO</div>

      <ul>
        <li><a href="#sobre" v-on:click="fechaNavbar()">Sobre</a></li>
        <li><a href="#beneficios" v-on:click="fechaNavbar()">Beneficios</a></li>
        <li><a href="#midias" v-on:click="fechaNavbar()">Mídias</a></li>
        <li><a href="#contato" v-on:click="fechaNavbar()">Contatos</a></li>
      </ul>
    </nav>
  </header>
</template>
<script>
export default {
  data() {
    return {};
  },
  methods: {
    fechaNavbar() {
      let ul = document.querySelector("ul");
      let check = document.querySelector("#check");
      ul.style.left = "100%";
      check.checked = false;
    },
    abreNavbar() {
      let ul = document.querySelector("ul");
      let check = document.querySelector("#check");
      check.checked ? (ul.style.left = "0") : (ul.style.left = "100%");
    },
  },
};
</script>
<style scoped>
header {
  height: 60px;
  -webkit-box-shadow: -1px 2px 24px -6px rgba(0, 0, 0, 0.75);
  -moz-box-shadow: -1px 2px 24px -6px rgba(0, 0, 0, 0.75);
  box-shadow: -1px 2px 24px -6px rgba(0, 0, 0, 0.75);
}
nav {
  display: flex;
  justify-content: space-between;
  align-items: center;
  line-height: 60px;
  padding: 0 1em;
  max-width: 1260px;
  margin: 0 auto;
  width: 100%;
  background-color: rgba(#000000, 0.95);
}
.checkbtn {
  font-size: 30px;
  color: #2b468b;
  order: 3;
  line-height: 60px;
  cursor: pointer;
  display: none;
}
#check {
  display: none;
}
.logo {
  font-size: 1.4rem;
  font-weight: 700;
  color: #2b468b;
}
ul li {
  display: inline;
  margin: 10px;
}
ul li a {
  text-decoration: none;
  color: #2b468b;
}

@media screen and (max-width: 860px) {
  .checkbtn {
    display: block !important;
  }
  ul {
    position: fixed;
    width: 100vw;
    height: 100vh;
    /* background: rgba(#000000, 0.9); */
    background: rgba(43, 70, 139, 0.8) !important;
    top: 60px;
    left: 100%;
    text-align: center;
    transition: all 0.5s;
    backdrop-filter: blur(3.5px) !important;
    display: flex;
    flex-direction: column;
    justify-content: center;
  }
  li {
    display: flex !important;
    align-items: center;
    justify-content: center;
  }
  a {
    color: white !important;
    font-size: 1.8rem;
    font-weight: 600;
  }
  #check:checked ~ ul {
    left: 0;
  }
}
</style>