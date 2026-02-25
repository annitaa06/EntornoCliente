<template>
  <section class="hero">
    <div class="hero-content">
      <div class="hero-text">
        <h1>Hola, soy <span class="highlight">Anna</span> 👋</h1>
        <p class="subtitle">Estudiante de Desarrollo de Aplicaciones Web</p>
        <p class="description">
          Me encanta la tecnología y aprender cosas nuevas. 
  Estudio Desarrollo de Aplicaciones Web, donde estoy adquiriendo conocimientos en HTML, CSS, JavaScript y Java. 
  Me gusta enfrentarme a nuevos retos y mejorar poco a poco.
        </p>
        <!-- BOTONES  -->
       <div class="hero-buttons">
  <button class="btn-primary" @click="$emit('irAProyectos')">
    Ver mis proyectos
  </button>
  
  <button class="btn-secondary" @click="$emit('irAContacto')">
    Contactar
  </button>
</div>
      </div>
      </div>

  </section>
</template>

<style scoped>
.hero {
  display: flex;
  align-items: center;
  justify-content: center;
  min-height: 70vh;
  padding: 40px;
}

.hero-content {
  display: flex;
  align-items: center;
  gap: 60px;
  max-width: 1000px;
  text-align: left;
}

.hero-text h1 {
  font-size: 3.5rem;
  margin-bottom: 10px;
}

.highlight { color: #42b883; }

.subtitle {
  font-size: 1.5rem;
  color: #666;
  font-weight: 500;
  margin-bottom: 20px;
}

.description {
  font-size: 1.1rem;
  color: #777;
  line-height: 1.6;
  margin-bottom: 30px;
}

.hero-buttons { display: flex; gap: 15px; }

.btn-primary {
  background: #42b883;
  color: white;
  padding: 12px 25px;
  border-radius: 8px;
  border: none;
  font-weight: bold;
  cursor: pointer;
}

.btn-secondary {
  background: white;
  color: #42b883;
  padding: 12px 25px;
  border-radius: 8px;
  border: 2px solid #42b883;
  font-weight: bold;
  cursor: pointer;
}

.hero-image .blob {
  width: 300px;
  height: 300px;
  background: #42b883;
  border-radius: 30% 70% 70% 30% / 30% 30% 70% 70%;
  display: flex;
  align-items: center;
  justify-content: center;
  animation: blob-anim 10s infinite alternate;
}

.hero-image img { width: 200px; }

@keyframes blob-anim {
  from { border-radius: 30% 70% 70% 30% / 30% 30% 70% 70%; }
  to { border-radius: 50% 50% 20% 80% / 25% 80% 20% 75%; }
}

/* Responsivo para móvil */
@media (max-width: 768px) {
  .hero-content { flex-direction: column-reverse; text-align: center; }
  .hero-buttons { justify-content: center; }
}
</style>