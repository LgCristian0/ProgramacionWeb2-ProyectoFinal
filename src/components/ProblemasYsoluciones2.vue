<!-- Referencias.vue -->
<template>
  <div class="Problemas_Y_Soluciones">
    <h1>¿Quienes pueden consumir SweetGuardPlus?</h1>
    <div class="cajas-container">
      <div class="caja">
        <h2>Individuos Preocupados por la Salud</h2>
        <p>Este grupo incluye a personas conscientes de los riesgos del consumo excesivo de azúcar refinado y que buscan alternativas más saludables. SweetGuard Plus atraerá a aquellos interesados en mantener niveles de azúcar en sangre estables y en reducir el riesgo de enfermedades relacionadas con el azúcar, como la diabetes tipo 2 y las enfermedades cardíacas.</p>
      </div>
      <div class="caja">
        <h2>Personas con Diabetes o Prediabetes</h2>
        <p>SweetGuard Plus puede ser especialmente relevante para aquellos que ya tienen diabetes o prediabetes, ya que ofrece una opción de endulzante natural que puede ayudar en la gestión de los niveles de azúcar en sangre.</p>
      </div>
      <div class="caja">
        <h2>Personas que Buscan Control de Peso</h2>
        <p>: Aquellas personas que están interesadas en reducir calorías en su dieta, ya sea para perder peso o mantenerlo, encontrarán atractivo el potencial de SweetGuard Plus para reducir la ingesta calórica sin sacrificar el sabor.</p>
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
.Problemas_Y_Soluciones {
  max-height: 100%;
  overflow-y: auto;
  text-align: center;
}
h1 {
  color: rgb(18, 112, 156);
  font-family: "American Typewriter", Helvetica, Arial, sans-serif;
}
.cajas-container {
  display: flex; /* Alinear cajas horizontalmente */
  justify-content: center; /* Centrar cajas horizontalmente */
  margin-top: 20px; /* Espaciado superior */
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
