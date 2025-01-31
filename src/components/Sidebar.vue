<template>
  <div class="sidebar">
    <h2>¡Bienvenido!</h2>
    <h3>Nombre: {{ registrarStore.nombre }}</h3>
    <h3>Correo: {{ registrarStore.email }}</h3>
    <ul>
      <li>
        <router-link to="/Contador"> Contador </router-link>
      </li>
      <li>
        <router-link to="/lista-de-tareas"> Lista De Tareas </router-link>
      </li>
      <li>
        <router-link to="/registrar"> Registrar </router-link>
      </li>
    </ul>
  </div>
</template>
<script setup>
import { useRegistrarStore } from '@/modules/registro/stores/registrarStore'
const registrarStore = useRegistrarStore()
</script>
<style>
.sidebar {
  width: 200px;
  background-color: gray;
  padding: 20px;
}
</style>
