<script setup>
import { ref } from 'vue'



const misProyectos = [
  {
    id: 1,
    nombre: 'Piedra, Papel o Tijera',
    desc: 'Juego clásico adaptado a Vue. ¡Prueba tu suerte contra la máquina!',
    link: 'https://github.com/annitaa06/EntornoCliente/blob/main/piedraPapelTijera.html',
    tipo: 'juego'
  },
  {
    id: 2,
    nombre: 'Calculadora de notas',
    desc: 'Herramienta simple para calcular medias académicas al instante.',
    link: 'https://github.com/annitaa06/EntornoCliente/tree/main/Calculadora%20de%20notas',
    tipo: 'calculadora'
  }
]


</script>

<template>
  <section class="proyectos-seccion">
    <h2>📂 Mis Proyectos</h2>
    <p>Aquí puedes ver mi código en GitHub </p>

    <div class="contenedor-grid">
      <div v-for="p in misProyectos" :key="p.id" class="card">
        <div class="card-content">
          <h3>{{ p.nombre }}</h3>
          <p>{{ p.desc }}</p>
          
          <div class="botones">


            
            <a :href="p.link" target="_blank" class="btn-github">GitHub</a>
          </div>
        </div>
      </div>
    </div>

  </section>
</template>

<style scoped>
.proyectos-seccion {
  padding: 20px;
}

.contenedor-grid {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(280px, 1fr));
  gap: 20px;
  margin-top: 20px;
}

.card {
  border: 1px solid #ddd;
  border-radius: 12px;
  background: #fff;
  transition: box-shadow 0.3s;
  text-align: left;
}

.card:hover {
  box-shadow: 0 5px 15px rgba(0,0,0,0.1);
}

.card-content {
  padding: 20px;
}

.botones {
  margin-top: 15px;
  display: flex;
  gap: 10px;
}

.btn-demo {
  background-color: #42b883;
  color: white;
  border: none;
  padding: 8px 12px;
  border-radius: 6px;
  cursor: pointer;
}

.btn-github {
  background-color: #2c3e50;
  color: white;
  text-decoration: none;
  padding: 8px 12px;
  border-radius: 6px;
  font-size: 14px;
}

.visor-demo {
  margin-top: 40px;
  padding: 20px;
  background: #f0fdf4;
  border-radius: 15px;
  border: 2px dashed #42b883;
}

.btn-cerrar-flotante {
  margin-top: 15px;
  background: none;
  border: 1px solid #999;
  padding: 5px 10px;
  border-radius: 4px;
  cursor: pointer;
  color: #666;
}

hr {
  border: 0;
  border-top: 1px solid #42b883;
  margin-bottom: 20px;
}
</style>