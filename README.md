# WINNERZAPOPAN.io
/ (carpeta raíz del repositorio)
│
├── index.html
├── style.css
└── script.js
└── /images  ← aquí pondrás tus imágenes (máximo 10)
<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Galería Mensual</title>
  <link rel="stylesheet" href="style.css">
</head>
<body>
  <header>
    <h1>Galería del Mes</h1>
    <p>Cambia las imágenes cada mes reemplazando los archivos en la carpeta <code>/images</code>.</p>
  </header>

  <main class="gallery">
    <!-- Puedes agregar hasta 10 imágenes -->
    <div class="image-card"><img src="images/img1.jpg" alt="Imagen 1"></div>
    <div class="image-card"><img src="images/img2.jpg" alt="Imagen 2"></div>
    <div class="image-card"><img src="images/img3.jpg" alt="Imagen 3"></div>
    <div class="image-card"><img src="images/img4.jpg" alt="Imagen 4"></div>
    <div class="image-card"><img src="images/img5.jpg" alt="Imagen 5"></div>
    <div class="image-card"><img src="images/img6.jpg" alt="Imagen 6"></div>
    <div class="image-card"><img src="images/img7.jpg" alt="Imagen 7"></div>
    <div class="image-card"><img src="images/img8.jpg" alt="Imagen 8"></div>
    <div class="image-card"><img src="images/img9.jpg" alt="Imagen 9"></div>
    <div class="image-card"><img src="images/img10.jpg" alt="Imagen 10"></div>
  </main>

  <footer>
    <p>© <span id="year"></span> Galería Mensual</p>
  </footer>

  <script src="script.js"></script>
</body>
</html>
@import url('https://fonts.googleapis.com/css2?family=Poppins:wght@400;600&display=swap');

body {
  margin: 0;
  font-family: 'Poppins', sans-serif;
  background: linear-gradient(135deg, #1e1e2f, #2b2b40);
  color: white;
  display: flex;
  flex-direction: column;
  min-height: 100vh;
}

header {
  text-align: center;
  padding: 2rem 1rem;
}

h1 {
  font-size: 2.5rem;
  margin-bottom: 0.5rem;
}

.gallery {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px, 1fr));
  gap: 20px;
  padding: 20px;
  flex-grow: 1;
}

.image-card {
  position: relative;
  overflow: hidden;
  border-radius: 20px;
  box-shadow: 0 5px 20px rgba(0,0,0,0.4);
  transition: transform 0.3s ease, box-shadow 0.3s ease;
}

.image-card img {
  width: 100%;
  height: 100%;
  object-fit: cover;
  transition: transform 0.4s ease;
}

.image-card:hover {
  transform: scale(1.05);
  box-shadow: 0 8px 30px rgba(0,0,0,0.6);
}

.image-card:hover img {
  transform: scale(1.1);
  filter: brightness(1.1);
}

footer {
  text-align: center;
  padding: 1rem;
  font-size: 0.9rem;
  background-color: rgba(255,255,255,0.05);
}
// Actualiza el año automáticamente
document.getElementById("year").textContent = new Date().getFullYear();

// Puedes agregar funciones aquí más adelante (como efectos o slideshow)
