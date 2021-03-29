<template>
  <Navbar />
  <div class="wrapper">
    <div class="conteudo--wrapper">
      <div class="textos--conteudo--wrapper">
        <div class="titulo--textos">
          <h1>Trabalhe de casa</h1>
        </div>
        <div class="barra"></div>
        <div class="texto--conteudo">
          <p>
            Morbi at tellus nec magna consequat faucibus. In hac habitasse
            platea dictumst. Integer hendrerit dui ipsum, elementum porta nulla
            interdum sit amet. Aenean a malesuada enim. Nunc odio mauris,
            rhoncus ac sodales et, malesuada quis lorem. Sed eleifend arcu
            lacus, sed fringilla orci iaculis id.
          </p>
        </div>
        <div class="btn">
          <a href="#" class="btn--conteudo">Saiba mais</a>
        </div>
      </div>
    </div>

    <div class="img--wrapper">
      <div class="img">
        <img src="../assets/6534.jpg" alt="" />
      </div>
    </div>
  </div>
</template>
<script>
import Navbar from "./Navbar";
export default {
  components: {
    Navbar,
  },
};
</script>
<style scoped>
.wrapper {
  height: calc(100vh - 60px);
  display: flex;
}
.wrapper > div {
  /* border: 1px solid red; */
  width: 100%;
}
.conteudo--wrapper {
  display: flex;
  align-items: center;
  padding: 1em;
}
.textos--conteudo--wrapper {
  padding: 4em;
}
.titulo--textos {
  margin-bottom: 0.8em;
}
.titulo--textos h1 {
  font-size: 4rem;
  color:  #2B468B;
  transition: .3s ease-in-out;
}
.texto--conteudo {
  text-align: justify;
  color: #253765;
}
.btn {
  margin-top: 40px;
}
.btn--conteudo {
  padding: 10px 20px;
   border-radius: 20px;
  text-decoration: none;
  color: white;
  /* background: #ff4f5a; */
  background: #2B468B;
  transition: .2s ease-in-out;
 
}
.btn--conteudo:hover{
 background: #253765;
}
.barra {
  /* border: 1px solid #ff4f5a;  */
  border: 1px solid #2B468B;
  width: 80%;
  margin-bottom: 1em;
}
.img--wrapper {
  display: flex;
  align-items: center;
  justify-content: center;
  padding: 1em;
  width: 100%;
  /* border: 1px solid; */
  padding: 4em 0;
  transition: .3s ease;
}
.img--wrapper .img {
  /* background: url(https://image.freepik.com/vetores-gratis/ilustracao-do-conceito-de-teletrabalho_114360-1600.jpg) no-repeat; 
     background: url(https://image.freepik.com/vetores-gratis/mulher-investindo-e-obtendo-lucro_74855-11229.jpg) no-repeat;
    background-size: cover;
    background-position: center;
     border: 1px solid yellow; 
    height: 100%;
    width: 100%;*/
  /* height: 100%;
    width: 100%; */
}
.img img {
  width: 100%;
  min-width: 400px;
}
@media screen and (max-width: 860px) {
  .img--wrapper {
    display: none;
  }
}
@media screen and (max-width: 460px) {
    .conteudo--wrapper{
        display: flex;
        align-items: center;
        justify-content: center;
    }
    .titulo--textos{
       text-align: center;
    }
  .titulo--textos h1{
      font-size: 2rem  !important;
  }
  .barra{
      width: 100%;
  }
  .texto--conteudo{
      text-align: center;
  }
.textos--conteudo--wrapper{
      display: flex;
      justify-content: center;
      align-items: center;
      flex-direction: column;
  }
  
}
</style>