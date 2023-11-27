<!-- Referencias.vue -->
<template>
  <div class="sobreNosotros">
    <h1>Sobre Nosotros</h1>
    <div class="cajas-container">
      <div class="caja">
        <h2>Historia y Visión</h2>
        <p>En SWEETGUARD PLUS, nuestra historia comienza con la búsqueda de una solución innovadora para abordar las necesidades nutricionales de las personas con diabetes. Y estamos comprometidos con la creación de un cambio positivo en la salud y el bienestar.</p>
      </div>
      <div class="caja">
        <h2>Compromiso con la Salud y la Sostenibilidad</h2>
        <p>En el corazón de SWEETGUARD PLUS está nuestro compromiso con la salud y la sostenibilidad. Nuestra tecnología libera gradualmente el jarabe de Yacón en el cuerpo, manteniendo niveles de azúcar en sangre estables y reduciendo calorías de manera inteligente</p>
      </div>
      <div class="caja">
        <h2>Equipo Apasionado y Comprometido</h2>
        <p> SWEETGUARD PLUS está formado por un equipo de estudiantes apasionados que comparten la visión de mejorar la vida de las personas. Desde expertos en ingenieria quimica, alimentos, industrial, informatica hasta entusiastas de la salud, cada miembro aporta su perspectiva única para hacer de este proyecto una realidad.</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  // Lógica específica del componente de referencias
};
</script>

<style scoped>
.sobreNosotros {
  max-height: 100%;
  overflow-y: auto;
  text-align: center;
}
h1 {
  color: rgb(219, 34, 9);
  font-family: "Comic Sans MS", Helvetica, Arial, sans-serif;
  text-align: center;
}

.cajas-container {
  display: flex; /* Alinear cajas horizontalmente */
  justify-content: center; /* Centrar cajas horizontalmente */
  margin-top: 20px; /* Espaciado superior */
  text-align: center;
}

.caja {
  border: 1px solid #ccc;
  padding: 20px;
  margin: 0 10px; /* Espaciado entre cajas */
  width: 400px; /* Ancho máximo de cada caja */
  text-align: center; /* Alinea el texto al inicio dentro de la caja */
  
}

.caja h2 {
  color: blue; /* Estilo del título de la caja */
}
</style>
