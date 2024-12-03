<script setup>
import { ref, computed } from 'vue';
const nombre = ref('Thalia');
const apellido = ref('Bravo');
const nomComplet = computed(() => `${nombre.value} ${apellido.value}`);
</script>
<template>
    <div>
        <p>Nom complet: {{ nomComplet }}</p>
        <input v-model="nombre" placeholder="Nombre" />
        <input v-model="apellido" placeholder="Apellido" />
    </div>
</template>
