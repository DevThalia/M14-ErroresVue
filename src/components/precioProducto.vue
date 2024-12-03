<template>
    <input v-model.number="minPrecio" placeholder="Preu mínim" />
    <ul>
        <li v-for="producto in listaFiltrada" :key="productos.nombre">
            {{ producto.nombre }} - {{ producto.precio }} €
        </li>
    </ul>
</template>

<script setup>
import { ref, computed } from 'vue';
const productos = ref([
  { nombre: 'Portatil', precio: 1000 },
  { nombre: 'Movil', precio: 500 },
  { nombre: 'Tablet', precio: 300 },
]);

const minPrecio = ref('')

const listaFiltrada = computed (()=>
    productos.value.filter(producto=>producto.precio>=minPrecio.value)
);

</script>