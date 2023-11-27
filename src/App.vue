<template>
  <div id="app">
    <header class="header">
      <div class="logo-container">
        <img
          src="./imagenes/vector-degradado-logotipo-colorido-pajaro_343694-1365.avif"
          alt="SweetGuardPlus Logo"
        />
      </div>
      <div class="product-details">
        <h1>SweetGuardPlus</h1>
      </div>
      <div class="product-info">
        <div class="product-image">
          <img src="./imagenes/logo1.jpg" alt="SweetGuardPlus Product" />
        </div>
      </div>
    </header>
    <div class="botones">
      <nav class="menu">
        <button @click="mostrarComponente('sobrenosotros')">
          Sobre nostros
        </button>
        <button @click="mostrarComponente('problemasysoluciones')">
          Problemas y soluciónes
        </button>
        <button @click="mostrarComponente('ventajacompetitiva')">
          Ventaja Competitiva
        </button>
        <button @click="mostrarComponente('problemasysoluciones2')">
          Publico objetivo
        </button>
      </nav>
    </div>
    <div>
      <div class="contenido">
        <component :is="componenteActual" />
      </div>
    </div>
    <div class="nuevos-botones">
      <button @click="mostrarComponente('infextra')">
        ¿Te gustaria saber más del producto?
      </button>
      <button @click="mostrarComponente('calculadora')">Calculadora</button>
      <button @click="mostrarComponente('tiendaEnLinea')">
        Tienda en línea
      </button>
    </div>

    <footer class="footer">
      <div class="redes-sociales">
        <a
          href="https://www.facebook.com/medicinaumssoficial?locale=es_LA"
          target="_blank"
          rel="noopener noreferrer"
        >
          <img
            src="https://upload.wikimedia.org/wikipedia/commons/thumb/5/51/Facebook_f_logo_%282019%29.svg/2048px-Facebook_f_logo_%282019%29.svg.png"
            alt="Facebook"
          />
        </a>
        <a
          href="https://twitter.com/MedanosGE"
          target="_blank"
          rel="noopener noreferrer"
        >
          <img
            src="https://bayrivercolleges.ca/files/logo-x-twitter.svg"
            alt="Twitter"
          />
        </a>
        <!-- Agrega más enlaces a otras redes sociales si es necesario -->
      </div>
      <p>&copy; 2023 SweetGuardPlus. Todos los derechos reservados.</p>
    </footer>
    <!-- Otros componentes y contenido de la aplicación van aquí -->
  </div>
</template>

<script>
//Importacion de componentes
import ProblemasYsoluciones from "./components/ProblemasYsoluciones.vue";
import ProblemasYsoluciones2 from "./components/ProblemasYsoluciones2.vue";
import SobreNosotros from "./components/SobreNosotros.vue";
import VentajaCompetitiva from "./components/VentajaCompetitiva.vue";
import Calculadora from "./components/Calculadora.vue";
import Infextra from "./components/Infextra.vue";
import TiendaEnLinea from "./components/TiendaEnLinea.vue";

export default {
  data() {
    return {
      componenteActual: null,
    };
  },
  methods: {
    mostrarComponente(nombre) {
      switch (nombre) {
        case "sobrenosotros":
          this.componenteActual = SobreNosotros;
          break;
        case "problemasysoluciones":
          this.componenteActual = ProblemasYsoluciones;
          break;
        case "ventajacompetitiva":
          this.componenteActual = VentajaCompetitiva;
          break;
        case "problemasysoluciones2":
          this.componenteActual = ProblemasYsoluciones2;
          break;
        case "calculadora":
          this.componenteActual = Calculadora;
          break;
        case "infextra":
          this.componenteActual = Infextra;
          break;
        case "tiendaEnLinea":
          this.componenteActual = TiendaEnLinea;
          break;
        default:
          this.componenteActual = null;
      }
    },
  },
};
</script>

<style>
body {
  margin: 0;
  font-family: "Comic Sans MS", Helvetica, Arial, sans-serif;
}

.header {
  background-image: url("./imagenes/logo.jpg");
  background-size: 1080px 400px;
  color: #fff;
  padding: 50px;
  display: flex;
  justify-content: space-between;
  align-items: center;
  transition: transform 10s;
}

.logo-container img {
  width: 100px;
  height: 100px;
  border-radius: 50%; /* Para hacer la imagen circular */
  transition: transform 0.3s;
}

.logo-container img:hover {
  transform: rotate(360deg);
}

.product-info {
  display: flex;
  align-items: center; /* Alinea los elementos verticalmente */
}

.product-image img {
  width: 120px;
  height: 120px;
  border-radius: 10px;
}

.product-details {
  margin-left: 20px;
}

h1 {
  font-size: 1.5em;
  margin-bottom: 10px;
}

.product-details h1 {
  font-size: 4em;
  margin-bottom: 10px;
  font-family: "Brush Script MT", sans-serif;
  color: #ff6600;
  text-shadow: 2px 2px 4px rgba(0, 0, 0, 0.5);
  transition: color 0.3s, text-shadow 0.3s;
}

.product-details h1:hover {
  color: #f8f8f4; /* Cambia el color al pasar el ratón sobre el texto */
  text-shadow: 4px 4px 6px rgba(0, 0, 0, 0.7);
}
.menu {
  display: flex;
  justify-content: center;
}

.menu button {
  margin: 0 10px;
  padding: 10px;
  font-size: 1em;
  background-color: #fc3333;
  color: #fff;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  margin-top: 5px;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
  transition: background-color 0.3s, transform 0.3s, color 0.3s;
}

.menu button:hover {
  background-color: #570404;
  color: #fff;
  transform: scale(1.1);
  box-shadow: 0 8px 12px rgba(0, 0, 0, 0.2);
}

.botones {
  background-color: #f1241d;
  height: 50px;
}
.contenido {
  width: 100%;
  height: 100%; /* Puedes ajustar la altura según tus necesidades */
  border: 1px solid #e43232;
  overflow-y: auto; /* Agrega una barra de desplazamiento si el contenido excede la altura */
}
.nuevos-botones {
  display: flex;
  justify-content: center;
  background-color: #fc3333;
}

.nuevos-botones button {
  margin: 5px 20px;
  padding: 10px;
  font-size: 1em;
  background-color: #d32020;
  color: #fff;
  border: none;
  border-radius: 5px;
  cursor: pointer;
  transition: background-color 0.3s, transform 0.3s;
  box-shadow: 0 4px 6px rgba(0, 0, 0, 0.1);
}

.nuevos-botones button:hover {
  background-color: #570404;
  color: #fff;
  transform: scale(1.1);
  box-shadow: 0 8px 12px rgba(0, 0, 0, 0.2);
}

.footer {
  background-color: #333;
  color: #fff;
  padding: 20px;
  text-align: center;
}

.redes-sociales {
  display: flex;
  justify-content: center;
  margin-bottom: 10px;
}

.redes-sociales a {
  display: inline-block;
  margin: 0 10px;
}

.redes-sociales img {
  width: 30px; /* Ajusta el tamaño de los iconos según tus preferencias */
  height: 30px;
  transition: transform 0.3s;
}

.redes-sociales img:hover {
  transform: rotate(15deg);
}
</style>
