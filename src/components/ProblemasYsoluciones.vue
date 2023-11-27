<template>
  <div class="problemasysoluciones">
    <h1>Problemas y Soluciones</h1>
    <div class="cajas-container">
      <div class="caja">
        <h2>Descripción del problema identificado</h2>
        <p>
          El problema identificado es la prevalencia de enfermedades
          relacionadas con el azúcar, como la diabetes, la obesidad y las
          enfermedades cardíacas, debido al alto consumo de azúcar refinado en
          la dieta global. El azúcar refinado, ampliamente utilizado en
          alimentos y bebidas procesadas, contribuye significativamente a los
          desafíos de salud pública actuales.
        </p>
        <img
          src="../imagenes/problema.jpeg"
          alt="Imagen Descripción Problema 1"
          style="width: 100%; height: 40%"
        />
      </div>
      <div class="caja">
        <h2>Solución al problema identificado</h2>
        <p>
          Nuestra solución se basa en el desarrollo de un proceso de
          microencapsulación que permite extraer y encapsular los
          fructooligosacáridos (FOS), el endulzante natural presente en el
          yacón. Este proceso garantiza que la dulzura se libere de manera
          gradual en el organismo, evitando los picos de azúcar en sangre. El
          resultado es un endulzante natural de yacón que puede utilizarse en
          una variedad de productos, desde bebidas hasta productos horneados,
          sin comprometer la salud de las personas con diabetes.
        </p>
        <img
          src="../imagenes/producto.jpg"
          alt="Imagen Descripción Solución 1"
          style="width: 100%; height: auto"
        />
      </div>
    </div>
  </div>
</template>

<script>
export default {
  // Lógica específica del componente de problemas y soluciones
};
</script>

<style scoped>
.problemasysoluciones {
  max-height: 100%;
  overflow-y: auto;
  text-align: center; /* Alinea el texto al centro */
}

h1 {
  color: rgb(214, 15, 1);
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
