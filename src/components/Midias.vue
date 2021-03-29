<template>
  <div class="conteudo--midias" id="midias">
    <div class="texto--midias">
      <h1>Também estou nas redes sociais</h1>
    </div>
    <div class="icons">
        <a href="" class="icon"><i class="fab fa-facebook-f"></i></a>
        <a href="" class="icon"><i class="fab fa-youtube"></i></a>
        <a href="" class="icon"><i class="fab fa-instagram"></i></a>
    </div>
  </div>
</template>
<script>
export default {};
</script>
<style scoped>
#midias{
    padding: 4em;
}
.texto--midias{
    text-align: center;
    padding-bottom: 15px;
}
.texto--midias h1{
    color: #2B468B;
}
.icons{
    display: flex;
    justify-content: center;
    align-items: center;
    flex-wrap: wrap;
}
.icons>a{
    flex: 1;
    padding:3em;
    text-align: center;
    border: 1px solid;
    margin: 10px;
    border-radius: 15px;
    cursor: pointer;
    text-decoration: none;
    color:#2b468b ;
    transition: .3s ease-in-out;
}
.icons>a i{
    font-size: 2rem;
}
.icons>a:hover{
    color: white;
    background: #2b468b;
}
</style>