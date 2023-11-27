<template>
  <div>
    <h2 class="titulo">Bienvenido a la Tienda en Línea</h2>
    <div v-for="(producto, index) in productos" :key="index" class="producto">
      <img
        :src="producto.imagen"
        :alt="producto.nombre"
        class="imagen-producto"
      />
      <div class="info-producto">
        <h3 class="nombre">{{ producto.nombre }}</h3>
        <p class="descripcion">{{ producto.descripcion }}</p>
        <p class="precio">Precio: ${{ producto.precio.toFixed(2) }}</p>
        <button @click="agregarAlCarrito(index)" class="boton-agregar">
          Agregar al carrito
        </button>
      </div>
    </div>

    <div class="carrito" :class="{ 'carrito-vacio': carrito.length === 0 }">
      <h3>Carrito de Compras</h3>
      <ul v-if="carrito.length > 0">
        <li v-for="(item, index) in carrito" :key="index" class="item-carrito">
          {{ item.nombre }} - Cantidad: {{ item.cantidad }}
        </li>
      </ul>
      <p class="total">Total: ${{ calcularTotal().toFixed(2) }}</p>
      <button
        @click="comprar"
        :disabled="carrito.length === 0"
        class="boton-comprar"
      >
        Comprar
      </button>
      <p v-if="carrito.length === 0" class="mensaje-carrito-vacio">
        Tu carrito está vacío
      </p>
    </div>
  </div>
</template>
<script>
import img from "../imagenes/producto.jpg";
export default {
  data() {
    return {
      productos: [
        {
          nombre: "SweetGuard Plus ",
          descripcion:
            '"SweetGuard Plus”: Endulzante natural a base de microcápsulas de jarabe de Yacón',
          imagen: img,
          precio: 10.0,
        },
        // Agrega más productos según sea necesario
      ],
      carrito: [],
    };
  },
  methods: {
    agregarAlCarrito(index) {
      const producto = this.productos[index];
      const itemEnCarrito = this.carrito.find(
        (item) => item.nombre === producto.nombre
      );

      if (itemEnCarrito) {
        itemEnCarrito.cantidad += 1;
      } else {
        this.carrito.push({
          nombre: producto.nombre,
          cantidad: 1,
        });
      }
    },
    calcularTotal() {
      return this.carrito.reduce((total, item) => {
        const producto = this.productos.find((p) => p.nombre === item.nombre);
        return total + producto.precio * item.cantidad;
      }, 0);
    },
    comprar() {
      console.log(
        "¡Compra realizada! Total: $",
        this.calcularTotal().toFixed(2)
      );

      this.carrito = [];
    },
  },
};
</script>
<style scoped>
.titulo {
  font-family: "Brush Script MT", sans-serif;
  text-align: center;
  color: #333;
  font-size: 38px;
  margin-bottom: 20px;
}
.producto {
  background-image: url("../imagenes/fondo3.jpg");
  display: flex;
  margin-bottom: 30px;
  border: 2px solid #000000;
  padding: 10px;
  border-radius: 20px;
  transition: transform 0.3s;
}
.producto:hover {
  transform: scale(1.05);
}
.imagen-producto {
  width: 100px;
  height: 100px;
  object-fit: cover;
  margin-right: 10px;
  border-radius: 8px;
}
.info-producto {
  flex-grow: 1;
}
.nombre {
  font-size: 18px;
  margin-bottom: 5px;
  color: #050505;
}
.descripcion {
  color: #fffafa;
}
.precio {
  color: #080808;
  font-weight: bold;
}
.boton-agregar {
  background-color: #008000;
  color: #fff;
  border: none;
  padding: 8px 15px;
  cursor: pointer;
  border-radius: 5px;
  transition: background-color 0.3s;
}
.boton-agregar:hover {
  background-color: #070807;
}
.carrito {
  background-image: url("../imagenes/fondo5.jpg");
  margin-top: 30px;
  border: 1px solid #ddd;
  padding: 20px;
  border-radius: 8px;
}
.carrito-vacio {
  background-color: #f9f9f9;
}
.item-carrito {
  margin-bottom: 10px;
  color: #0f0d0d;
}
.total {
  font-weight: bold;
  margin-top: 10px;
  color: #333;
}
.boton-comprar {
  background-color: #008000;
  color: #fff;
  border: none;
  padding: 10px;
  cursor: pointer;
  border-radius: 5px;
  transition: background-color 0.3s;
}
.boton-comprar:hover {
  background-color: #004d00;
}
.mensaje-carrito-vacio {
  color: #0e0c0c;
  text-align: center;
  margin-top: 10px;
}
</style>
