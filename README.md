<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>Mi portafolio</title>
<link rel="preconnect" href="https://fonts.googleapis.com">
<link rel="preconnect" href="https://fonts.gstatic.com" crossorigin>
<link href="https://fonts.googleapis.com/css2?family=Bricolage+Grotesque:wght@500;700;800&family=DM+Sans:wght@400;500&display=swap" rel="stylesheet">
  
<script>
const PORTAFOLIO = {
  nombre: "SpaceCat-2008",
  titulo: "El arte empieza donde termina el cielo 😼",
  presentacion: "Aprendiendo java y creando Ideas.",
  foto: "",   // opcional: pon el nombre de tu foto subida al repo, por ejemplo "foto.jpg"

  proyectos: [
    {
      nombre: "Mini Juego 2D",
      descripcion: "Pequeño proyecto de un mini juego para <Aliens Cat Survival 3D",
      tecnologias: ["Java"],
      enlace: "https://github.com/SpaceCat-2008/Alien-moon-survival-2D/",
      demo: "[https://spacecat-2008.github.io/Alien-moon-survival-2D/]"
    }
  ],

  habilidades: ["HTML","Python"],

  contacto: {
    email: "matias.f.g.lppn@gmail.com",
    github: "[https://github.com/SpaceCat-2008]",
    linkedin: ""
  }
};
</script>

<style>
:root {
  --fondo: #F1F3F8;
  --superficie: #FFFFFF;
  --tinta: #1A2236;
  --tinta-suave: #54607A;
  --linea: #D5DAE6;
  --acento: #2B50F5;
  --acento-texto: #FFFFFF;
  --resalte: #FFD84D;
  --resalte-texto: #1A2236;
}
@media (prefers-color-scheme: dark) {
  :root {
    --fondo: #12172A;
    --superficie: #1B2240;
    --tinta: #EEF1FA;
    --tinta-suave: #A3AECB;
    --linea: #2C3558;
    --acento: #7C9BFF;
    --acento-texto: #12172A;
  }
}
* { box-sizing: border-box; margin: 0; padding: 0; }
html { scroll-behavior: smooth; }
body {
  background: var(--fondo);
  color: var(--tinta);
  font-family: "DM Sans", system-ui, sans-serif;
  font-size: 1.05rem;
  line-height: 1.65;
}
a { color: inherit; }
:focus-visible { outline: 3px solid var(--acento); outline-offset: 3px; }
.contenedor { max-width: 860px; margin: 0 auto; padding: 0 24px; }

/* Menú */
nav { padding: 24px 0; }
nav .contenedor { display: flex; justify-content: space-between; align-items: center; gap: 16px; }
nav .logo { font-family: "Bricolage Grotesque", sans-serif; font-weight: 800; text-decoration: none; }
nav ul { display: flex; gap: 22px; list-style: none; }
nav ul a { text-decoration: none; color: var(--tinta-suave); font-weight: 500; }
nav ul a:hover { color: var(--acento); }

/* Portada */
.portada { padding: 72px 0 88px; }
.portada .fila { display: flex; gap: 40px; align-items: center; justify-content: space-between; }
.portada h1 {
  font-family: "Bricolage Grotesque", sans-serif;
  font-weight: 800;
  font-size: clamp(2.8rem, 9vw, 5.6rem);
  line-height: 1;
  letter-spacing: -0.03em;
}
.portada h1 span {
  background: var(--resalte);
  color: var(--resalte-texto);
  padding: 0 .12em;
  border-radius: 6px;
  box-decoration-break: clone;
  -webkit-box-decoration-break: clone;
}
.portada .titulo {
  margin-top: 20px;
  font-family: "Bricolage Grotesque", sans-serif;
  font-size: clamp(1.15rem, 3vw, 1.5rem);
  font-weight: 500;
  color: var(--tinta-suave);
}
.portada .intro { margin-top: 20px; max-width: 54ch; color: var(--tinta-suave); }
.portada img {
  width: 170px; height: 170px; object-fit: cover;
  border-radius: 50%; border: 4px solid var(--resalte); flex-shrink: 0;
}
.botones { margin-top: 32px; display: flex; gap: 12px; flex-wrap: wrap; }
.boton {
  display: inline-block; padding: 12px 22px; border-radius: 999px;
  background: var(--acento); color: var(--acento-texto);
  font-weight: 500; text-decoration: none; transition: transform .15s;
}
.boton:hover { transform: translateY(-2px); }
.boton.secundario { background: transparent; color: var(--tinta); border: 1.5px solid var(--linea); }

/* Secciones */
section { padding: 64px 0; border-top: 1px solid var(--linea); }
h2 {
  font-family: "Bricolage Grotesque", sans-serif;
  font-size: clamp(1.8rem, 5vw, 2.4rem);
  letter-spacing: -0.02em;
  margin-bottom: 32px;
}

/* Proyectos: filas, no tarjetas idénticas */
.proyecto {
  display: grid; grid-template-columns: 1fr auto; gap: 8px 32px;
  padding: 28px 0; border-bottom: 1px solid var(--linea);
}
.proyecto:first-of-type { padding-top: 0; }
.proyecto h3 { font-family: "Bricolage Grotesque", sans-serif; font-size: 1.4rem; }
.proyecto p { color: var(--tinta-suave); max-width: 56ch; grid-column: 1; }
.etiquetas { display: flex; gap: 8px; flex-wrap: wrap; margin-top: 10px; grid-column: 1; }
.etiquetas span {
  font-size: .85rem; padding: 2px 12px; border-radius: 999px;
  background: var(--superficie); border: 1px solid var(--linea); color: var(--tinta-suave);
}
.enlaces { grid-column: 2; grid-row: 1 / span 3; display: flex; flex-direction: column; gap: 8px; align-items: flex-end; }
.enlaces a { color: var(--acento); font-weight: 500; text-underline-offset: 4px; }

/* Habilidades */
.habilidades { display: flex; flex-wrap: wrap; gap: 10px; list-style: none; }
.habilidades li {
  padding: 8px 18px; border-radius: 10px;
  background: var(--superficie); border: 1px solid var(--linea); font-weight: 500;
}

/* Contacto */
.contacto p { max-width: 50ch; color: var(--tinta-suave); margin-bottom: 20px; }
footer { padding: 40px 0; color: var(--tinta-suave); font-size: .9rem; border-top: 1px solid var(--linea); }

@media (max-width: 640px) {
  nav ul { gap: 14px; font-size: .95rem; }
  .portada { padding: 40px 0 56px; }
  .portada .fila { flex-direction: column-reverse; align-items: flex-start; }
  .portada img { width: 120px; height: 120px; }
  .proyecto { grid-template-columns: 1fr; }
  .enlaces { grid-column: 1; grid-row: auto; flex-direction: row; gap: 18px; align-items: flex-start; margin-top: 8px; }
}
@media (prefers-reduced-motion: reduce) {
  html { scroll-behavior: auto; }
  .boton { transition: none; }
}
</style>
</head>
<body>

<nav>
  <div class="contenedor">
    <a class="logo" href="#inicio" id="logo"></a>
    <ul>
      <li><a href="#proyectos">Proyectos</a></li>
      <li><a href="#habilidades">Habilidades</a></li>
      <li><a href="#contacto">Contacto</a></li>
    </ul>
  </div>
</nav>

<header class="portada" id="inicio">
  <div class="contenedor fila">
    <div>
      <h1 id="nombre"></h1>
      <p class="titulo" id="titulo"></p>
      <p class="intro" id="presentacion"></p>
      <div class="botones">
        <a class="boton" href="#proyectos">Ver mis proyectos</a>
        <a class="boton secundario" href="#contacto">Contáctame</a>
      </div>
    </div>
    <img id="foto" alt="Mi foto" hidden>
  </div>
</header>

<main>
  <section id="proyectos">
    <div class="contenedor">
      <h2>Proyectos</h2>
      <div id="lista-proyectos"></div>
    </div>
  </section>

  <section id="habilidades">
    <div class="contenedor">
      <h2>Habilidades</h2>
      <ul class="habilidades" id="lista-habilidades"></ul>
    </div>
  </section>

  <section id="contacto" class="contacto">
    <div class="contenedor">
      <h2>Contacto</h2>
      <p>¿Tienes una idea, una oferta o solo quieres saludar? Escríbeme.</p>
      <div class="botones" id="botones-contacto"></div>
    </div>
  </section>
</main>

<footer>
  <div class="contenedor" id="pie"></div>
</footer>

<script>
// Este código arma la página con lo que escribiste arriba. No necesitas tocarlo.
(function () {
  const d = PORTAFOLIO;
  const $ = (id) => document.getElementById(id);
  const crear = (tag, texto, clase) => {
    const el = document.createElement(tag);
    if (texto) el.textContent = texto;
    if (clase) el.className = clase;
    return el;
  };

  document.title = d.nombre + " | Portafolio";
  $("logo").textContent = d.nombre;

  const h1 = $("nombre");
  h1.appendChild(crear("span", d.nombre));
  $("titulo").textContent = d.titulo;
  $("presentacion").textContent = d.presentacion;

  if (d.foto) {
    $("foto").src = d.foto;
    $("foto").hidden = false;
  }

  d.proyectos.forEach((p) => {
    const caja = crear("article", "", "proyecto");
    caja.appendChild(crear("h3", p.nombre));
    caja.appendChild(crear("p", p.descripcion));

    const etiquetas = crear("div", "", "etiquetas");
    p.tecnologias.forEach((t) => etiquetas.appendChild(crear("span", t)));
    caja.appendChild(etiquetas);

    const enlaces = crear("div", "", "enlaces");
    if (p.enlace) {
      const a = crear("a", "Código");
      a.href = p.enlace; a.target = "_blank"; a.rel = "noopener";
      enlaces.appendChild(a);
    }
    if (p.demo) {
      const a = crear("a", "Ver demo");
      a.href = p.demo; a.target = "_blank"; a.rel = "noopener";
      enlaces.appendChild(a);
    }
    caja.appendChild(enlaces);
    $("lista-proyectos").appendChild(caja);
  });

  d.habilidades.forEach((h) => $("lista-habilidades").appendChild(crear("li", h)));

  const c = d.contacto;
  const botones = $("botones-contacto");
  if (c.email) {
    const a = crear("a", "Escríbeme un correo", "boton");
    a.href = "mailto:" + c.email;
    botones.appendChild(a);
  }
  [["GitHub", c.github], ["LinkedIn", c.linkedin]].forEach(([n, url]) => {
    if (!url) return;
    const a = crear("a", n, "boton secundario");
    a.href = url; a.target = "_blank"; a.rel = "noopener";
    botones.appendChild(a);
  });

  $("pie").textContent = "© " + new Date().getFullYear() + " " + d.nombre;
})();
</script>
</body>
</html>
