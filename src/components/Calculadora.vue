
<template>
  
  <div class="calculator-container">
    
    <div class="inner-container">
      <h2 class="titulo">Calculadora del endulzante SweetGuardPlus</h2>
      <p>
        Convierte el azúcar en SweetGuard Plus en tus recetas o alimentos.
        ¿Quieres convertir tu receta favorita o endulzar tus alimentos en una versión con menos azúcar agregada?
        Simplemente selecciona la cantidad de azúcar que sueles utilizar en el menú de abajo.
        ¡Te diremos la cantidad de endulzante SWEETGUARD PLUS que puedes usar en lugar del azúcar!
      </p>

      <label for="cantidadAzucar">Cantidad de azúcar a reemplazar (g):</label>
      <input type="number" id="cantidadAzucar" v-model="cantidadAzucar" />

      <button @click="calcularEndulzante">Calcular</button>

      <p v-if="resultado !== null">Cantidad de SweetGuard Plus recomendada: {{ resultado }} ml</p>

      <div class="conversion-info">
        <p>Recuerda que: 5g de azúcar (1 cucharilla) equivale a 3 gotas (0.15ml) de SweetGuard Plus</p>
      </div>
    </div>
  </div>
</template>

<script>
export default {
  data() {
    return {
      cantidadAzucar: 0,
      resultado: null,
    };
  },
  methods: {
    calcularEndulzante() {
      // Lógica de cálculo (ajústala según tus necesidades)
      // Aquí, convertimos 5g de azúcar a 3 gotas de SweetGuard Plus (0.15ml).
      this.resultado = (this.cantidadAzucar / 5) * 0.15;
    },
  },
};
</script>

<style scoped>
.calculator-container {
  display: flex;
  justify-content: center;
  align-items: center;
  height: 100vh; /* Ajusta la altura al 100% de la altura de la ventana */
  background-color: #ffb6c1; /* Rosa */
}

.inner-container {
  padding: 20px;
  background-color: #fff; /* Blanco */
  border-radius: 8px;
  box-shadow: 0 0 10px rgba(0, 0, 0, 0.1);
  text-align: center;
}
.titulo {
        font-family: 'Brush Script MT', sans-serif;
        text-align: center;
        color: #333;
        font-size: 38px;
        margin-bottom: 20px;
    }
.calculator-container p {
  margin-bottom: 15px;
}

label {
  display: block;
  margin-bottom: 10px;
}

input {
  padding: 8px;
  font-size: 14px;
  width: 100%;
  box-sizing: border-box;
  margin-bottom: 10px;
}

button {
  padding: 10px;
  font-size: 14px;
  background-color: #d32020;
  color: #fff;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  transition: background-color 0.3s;
}

button:hover {
  background-color: #570404;
}

.calculator-container p {
  color: #333;
  margin-top: 10px;
}

.conversion-info {
  margin-top: 20px;
  font-size: 12px;
  color: #777;
}
</style>