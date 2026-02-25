<template>
  <section class="about">
    <h2>Sobre Mí</h2>
    <div class="about-container">
      <p>Estudiante de DAW enfocada en el desarrollo frontend. Me gusta crear interfaces limpias y fáciles de usar.</p>
      
      <h3>Mis Herramientas</h3>
      <div class="skills-grid">
        <div class="skill-card">HTML5</div>
        <div class="skill-card">CSS3</div>
        <div class="skill-card">JavaScript</div>
        <div class="skill-card">Vue.js</div>
        <div class="skill-card">Git / GitHub</div>
        <div class="skill-card">AWS</div>
      </div>
    </div>
  </section>
</template>

<style scoped>
.about { max-width: 800px; margin: 0 auto; padding: 40px; }
.skills-grid {
  display: flex;
  flex-wrap: wrap;
  gap: 15px;
  justify-content: center;
  margin-top: 20px;
}
.skill-card {
  background: white;
  border-bottom: 4px solid #42b883;
  padding: 15px 25px;
  border-radius: 8px;
  font-weight: bold;
  box-shadow: 0 4px 6px rgba(0,0,0,0.05);
}
</style>