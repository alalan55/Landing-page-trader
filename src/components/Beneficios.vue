<template>
  <div class="conteudo--beneficios" id="beneficios">
    <div class="texto--beneficio">
      <h1>Benefícios</h1>
    </div>

    <div class="icons--card">
      <div class="card">
        <div class="icon">
          <i class="fas fa-globe-americas"></i>
        </div>
        <div class="texto--card">
          <p>In hac habitasse platea dictumst. Pellentesque id lacus odio.</p>
        </div>
      </div>

      <div class="card">
        <div class="icon">
          <i class="fas fa-chart-line"></i>
        </div>
        <div class="texto--card">
          <p>In hac habitasse platea dictumst. Pellentesque id lacus odio.</p>
        </div>
      </div>

      <div class="card">
        <div class="icon">
          <i class="fas fa-user-shield"></i>
        </div>
        <div class="texto--card">
          <p>In hac habitasse platea dictumst. Pellentesque id lacus odio.</p>
        </div>
      </div>

      <div class="card">
        <div class="icon">
          <i class="fas fa-clipboard-list"></i>
        </div>
        <div class="texto--card">
          <p>In hac habitasse platea dictumst. Pellentesque id lacus odio.</p>
        </div>
      </div>
    </div>
  </div>
</template>
<script>
export default {};
</script>
<style scoped>
.texto--beneficio {
  margin-bottom: 15px;
}
.texto--beneficio h1 {
  color: #253765;
}
.conteudo--beneficios {
  padding: 4em;
  text-align: center;
}
.icon {
  margin-bottom: 1em;
}
.icon i {
  font-size: 4rem;
}
.icons--card {
  display: flex;
  flex-wrap: wrap;
}
.icons--card > div {
  flex: 1 1 250px;
  padding: 2%;
}
.card {
  border: 1px solid #2b468b;
  margin: 4px;
  border-radius: 15px;
  color: #2b468b;
}
</style>