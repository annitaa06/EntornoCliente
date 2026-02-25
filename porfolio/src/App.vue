<script setup>
//IMPORTAMOS LOS COMPONENTES
import { ref } from 'vue'
import Inicio from './components/Inicio.vue'
import SobreMi from './components/SobreMi.vue'
import Proyectos from './components/Proyectos.vue'
import Contacto from './components/Contacto.vue'

const seccionActiva = ref('inicio')
</script>

<template>
  <div class="app-container">
    <header class="main-header">
      <div class="logo">Mi Portafolio</div>
      <nav class="nav-menu">
        <button :class="{ activo: seccionActiva === 'inicio' }" @click="seccionActiva = 'inicio'">Inicio</button>
        <button :class="{ activo: seccionActiva === 'sobre-mi' }" @click="seccionActiva = 'sobre-mi'">Sobre Mí</button>
        <button :class="{ activo: seccionActiva === 'proyectos' }" @click="seccionActiva = 'proyectos'">Proyectos</button>
        <button :class="{ activo: seccionActiva === 'contacto' }" @click="seccionActiva = 'contacto'">Contacto</button>
      </nav>
    </header>

    <main class="content">
  
  <Inicio 
    v-if="seccionActiva === 'inicio'" 
    @irAProyectos="seccionActiva = 'proyectos'"
    @irAContacto="seccionActiva = 'contacto'"
  />

  <SobreMi v-else-if="seccionActiva === 'sobre-mi'" />
  <Proyectos v-else-if="seccionActiva === 'proyectos'" />
  <Contacto v-else-if="seccionActiva === 'contacto'" />
  
</main>
  </div>
</template>

<style>
/* Reset total para evitar sorpresas */
* { margin: 0; padding: 0; box-sizing: border-box; }

body {
  font-family: 'Segoe UI', Tahoma, Geneva, Verdana, sans-serif;
  background-color: #f4f7f6;
  color: #2c3e50;
}

.main-header {
  background-color: #42b883; /* El verde Vue brillante */
  height: 70px;
  width: 100%;
  position: fixed;
  top: 0;
  left: 0;
  display: flex;
  align-items: center;
  justify-content: space-between;
  padding: 0 50px;
  z-index: 1000;
  box-shadow: 0 4px 12px rgba(0,0,0,0.1);
}

.logo {
  color: white;
  font-size: 1.5rem;
  font-weight: bold;
}

.nav-menu {
  display: flex;
  gap: 15px;
}

.nav-menu button {
  background: transparent;
  border: 2px solid transparent;
  color: white !important; /* Forzamos el color blanco para que se vea */
  padding: 8px 16px;
  cursor: pointer;
  font-weight: bold;
  font-size: 1rem;
  border-radius: 8px;
  transition: all 0.3s ease;
}

/* Efecto cuando pasas el ratón o la sección está activa */
.nav-menu button:hover, 
.nav-menu button.activo {
  background: rgba(255, 255, 255, 0.2);
  border-color: white;
}

.content {
  margin-top: 100px; /* Suficiente espacio para que no choque con el header */
  padding: 20px;
  width: 100%;
  max-width: 1200px;
  margin-left: auto;
  margin-right: auto;
  text-align: center;
}
</style>