<template>
  <div class="fale--comigo" id="contato">
    <div class="texto--fale--comigo">
      <h1>Quer saber mais sobre trade? Fale diretamente comigo</h1>
    </div>
    <form v-on:submit="enviaForm" id="formulario">
      <input
        type="text"
        placeholder="Nome e Sobrenome"
        v-model="nome"
        name="nome"
      />
      <input type="email" placeholder="E-mail" v-model="email" name="email" />

      <textarea
        name="mensagem"
        v-model="mensagem"
        cols="30"
        rows="10"
      ></textarea>

      <input type="submit" class="btn-enviar" value="Enviar" />
    </form>

    <div class="sucesso" v-if="success">
      <h1>Enviado com sucesso!</h1>
    </div>
  </div>
</template>
<script>
export default {
  data() {
    return {
      nome: "",
      email: "",
      mensagem: "",
      url: "http://localhost:3030/send",
      form: {},
      success: false,
    };
  },
  methods: {
    enviaForm(e) {
      // const formu = document.getElementById('formulario');
      e.preventDefault();
      this.form = {
        nome: this.nome,
        email: this.email,
        mensagem: this.mensagem,
      };

      let responseJson = JSON.stringify(this.form);
      // this.makeRequest(JSON.parse(responseJson));
      this.makeRequest(responseJson);
    },
    async makeRequest(val) {
      let response = await fetch(this.url, {
        method: "POST",
        mode: "cors",
        headers: {
          Accept: "application/json",
          "Content-Type": "application/json",
        },
        body: val,
      });
      const content = await response.json();
      // console.log(content.response);
      content.response.includes("OK")
        ? this.mensagemDeSucesso()
        : (this.success = false);
    },

    mensagemDeSucesso() {
      const formu = document.getElementById("formulario");
      let intervalo = setInterval(() => {
        this.success = true;
      }, 2000);

      setTimeout(() => {
        clearInterval(intervalo);
        this.success = false;
        formu.reset();
      }, 6000);
    },
  },
};
</script>
<style scoped>
.sucesso {
  /* border: 1px solid; */
  text-align: center;
  margin-top: 1.5%;
  background-color: #708bc9;
  /* background-color:#2E8B57; */
  border-radius: 15px;
  padding: 5px;
  transition: 0.4s ease-in-out;
}
.sucesso h1 {
  color: white;
}
.fale--comigo {
  padding: 4em;
  background: #ebf2fa;
}
.texto--fale--comigo {
  text-align: center;
  color: #253765;
  padding-bottom: 15px;
}
form {
  display: flex;
  flex-direction: column;
}
input {
  margin: 10px 0;
  padding: 10px;
  background: none;
  outline: 0;
  border: 1px solid #253765;
}
textarea {
  max-width: 100%;
  background: none;
  border: 1px solid #253765;
}
.btn-enviar {
  background: #253765;
  color: white;
  cursor: pointer;
  transition: 0.3s ease-in-out;
  padding: 10px;
}
.btn-enviar:hover {
  background: #405280;
}
</style>