<template>
  <section class="contacto-section">
    
    <div class="header-contacto">
      <h2>📬 ¿Hablamos?</h2>
      <p>Estoy buscando mi primera oportunidad como desarrolladora. ¡Escríbeme!</p>
    </div>

    <div class="grid-contacto">
      
      <a href="mailto:annarosafabregat1@gmail.com" class="card-contacto">
        <div class="icono">📧</div>
        <h3>Email</h3>
        <p>annarosafabregat1@gmail.com</p>
        <span class="action">Enviar mensaje →</span>
      </a>

      <a href="https://github.com/annitaa06" target="_blank" class="card-contacto">
        <div class="icono">🐙</div>
        <h3>GitHub</h3>
        <p>@annitaa06</p>
        <span class="action">Ver repositorios →</span>
      </a>

    </div>
  </section>
</template>

<style scoped>
/* Estilos generales de la sección */
.contacto-section {
  padding: 40px 20px;
  text-align: center;
  max-width: 1000px;
  margin: 0 auto; /* Centra la sección en la pantalla */
}

.header-contacto h2 {
  font-size: 2.5rem;
  margin-bottom: 10px;
  color: #2c3e50;
}

.header-contacto p {
  color: #666;
  font-size: 1.1rem;
  margin-bottom: 40px;
}

/* Configuración de la rejilla de tarjetas */
.grid-contacto {
  display: grid;

  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 20px; /* Espacio entre tarjetas */
}

/* Diseño individual de cada tarjeta */
.card-contacto {
  background: white;
  padding: 30px;
  border-radius: 15px;
  text-decoration: none;
  color: inherit;
  border: 1px solid #eee;
  /* 'transition' hace que los cambios al pasar el ratón (hover) sean suaves y no bruscos */
  transition: all 0.3s ease;
  box-shadow: 0 4px 6px rgba(0,0,0,0.02);
}

/* EFECTO HOVER: Lo que pasa cuando pones el ratón encima */
.card-contacto:hover {
  transform: translateY(-10px); /* La tarjeta "sube" 10 píxeles */
  border-color: #42b883; /* El borde cambia al verde de Vue */
  /* Añadimos una sombra más marcada para dar sensación de que flota */
  box-shadow: 0 10px 20px rgba(66, 184, 131, 0.1);
}

.icono {
  font-size: 2.5rem;
  margin-bottom: 15px;
}

.card-contacto h3 {
  margin-bottom: 5px;
  color: #42b883; /* Título de la tarjeta en verde */
}

.card-contacto p {
  font-size: 0.9rem;
  color: #7f8c8d;
  margin-bottom: 15px;
}

/* Estilo para el texto pequeño de acción ("Ver repositorios", etc) */
.action {
  font-weight: bold;
  font-size: 0.8rem;
  color: #2c3e50;
  text-transform: uppercase;
  letter-spacing: 1px; /* Separa un poco las letras para que quede más elegante */
}
</style>