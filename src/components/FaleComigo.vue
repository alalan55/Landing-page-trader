<template>
<div class="fale--comigo" id="contato">
    <div class="texto--fale--comigo">
        <h1>Quer saber mais sobre trade? Fale diretamente comigo</h1>
    </div>
    <form action="">


        <input type="text" placeholder="Nome e Sobrenome">
        <input type="email" placeholder="E-mail">

        <textarea name="" id="" cols="30" rows="10"></textarea>

        <input type="button"  class="btn-enviar" value="Enviar">
    </form>

</div>

</template>
<script>
export default {};
</script>
<style scoped>

.fale--comigo{
    padding: 4em;
    background: #EBF2FA;
}
.texto--fale--comigo{
    text-align: center;
    color: #253765;
    padding-bottom: 15px;
}
form{
    display: flex;
    flex-direction: column;
}
input{
    margin: 10px 0;
    padding: 10px;
    background: none;
    outline: 0;
    border: 1px solid #253765;
}
textarea{
    max-width: 100%;
    background: none;
    border: 1px solid #253765;
}
.btn-enviar{
    background:#253765;
    color: white;
    cursor: pointer;
    transition: .3s ease-in-out;
    padding: 10px;
}
.btn-enviar:hover{
   background: #405280;
}

</style>