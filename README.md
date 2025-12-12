<!doctype html>
<html lang="es">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width, initial-scale=1" />
  <title>Mi Página Web - Plantilla</title>
  <meta name="description" content="Plantilla limpia y moderna para sitio web personal o pequeño negocio." />
  <style>
    :root{
      --bg:#0f1724;
      --card:#0b1220;
      --muted:#9aa4b2;
      --accent:#7c3aed;
      --glass: rgba(255,255,255,0.04);
      --radius:14px;
      --max-width:1100px;
      --gap:20px;
      color-scheme: dark;
      font-family: Inter, ui-sans-serif, system-ui, -apple-system, "Segoe UI", Roboto, "Helvetica Neue", Arial;
    }
    *{box-sizing:border-box}
    body{
      margin:0;
      background: radial-gradient(1000px 600px at 10% 10%, rgba(124,58,237,0.12), transparent),
                  radial-gradient(800px 400px at 90% 80%, rgba(14,165,233,0.06), transparent),
                  var(--bg);
      color:#e6eef6;
      -webkit-font-smoothing:antialiased;
      -moz-osx-font-smoothing:grayscale;
      line-height:1.5;
      padding:32px 18px;
    }

    .container{max-width:var(--max-width);margin:0 auto;gap:var(--gap);display:flex;flex-direction:column}

    header{display:flex;align-items:center;justify-content:space-between;padding:14px 18px;background:linear-gradient(180deg, rgba(255,255,255,0.02), transparent);border-radius:12px;margin-bottom:24px}
    .brand{display:flex;gap:12px;align-items:center}
    .logo{width:44px;height:44px;border-radius:10px;display:grid;place-items:center;background:linear-gradient(135deg,var(--accent),#06b6d4);font-weight:700}
    nav{display:flex;gap:12px;align-items:center}
    nav a{color:var(--muted);text-decoration:none;padding:8px 12px;border-radius:8px}
    nav a:hover{color:var(--accent);background:var(--glass)}

    .hero{display:grid;grid-template-columns:1fr 420px;gap:28px;align-items:center;margin-bottom:28px}
    .card{background:linear-gradient(180deg, rgba(255,255,255,0.02), transparent);padding:22px;border-radius:var(--radius);box-shadow:0 6px 18px rgba(2,6,23,0.6)}
    .title{font-size:28px;margin:0 0 8px}
    .lead{color:var(--muted);margin:0 0 18px}
    .cta{display:inline-flex;gap:8px;align-items:center;padding:10px 14px;border-radius:10px;background:linear-gradient(90deg,var(--accent),#06b6d4);color:white;text-decoration:none;font-weight:600}

    .features{display:grid;grid-template-columns:repeat(3,1fr);gap:14px;margin-top:12px}
    .feature{padding:12px;border-radius:12px;background:rgba(255,255,255,0.02);}
    .feature h4{margin:0 0 6px}
    .feature p{margin:0;color:var(--muted);font-size:14px}

    .mock{border-radius:12px;overflow:hidden;background:linear-gradient(180deg,#061224, #021124);padding:16px}
    .mock img{width:100%;height:auto;display:block;border-radius:8px}

    .grid-3{display:grid;grid-template-columns:repeat(3,1fr);gap:16px;margin-bottom:24px}

    footer{display:flex;justify-content:space-between;align-items:center;padding:14px;color:var(--muted);margin-top:16px}

    /* responsive */
    @media (max-width:980px){
      .hero{grid-template-columns:1fr}
      .grid-3{grid-template-columns:repeat(2,1fr)}
    }
    @media (max-width:640px){
      nav{display:none}
      header{padding:12px}
      .grid-3{grid-template-columns:1fr}
    }

    /* simple form styles */
    form{display:flex;flex-direction:column;gap:12px}
    input,textarea{background:transparent;border:1px solid rgba(255,255,255,0.06);padding:10px;border-radius:8px;color:inherit}
    input::placeholder,textarea::placeholder{color:var(--muted)}
    button[type=submit]{cursor:pointer;padding:10px 14px;border-radius:10px;border:0;background:var(--accent);color:white;font-weight:600}

    /* small utilities */
    .muted{color:var(--muted)}
    .kbd{background:rgba(255,255,255,0.03);padding:6px 8px;border-radius:8px;font-size:13px}
  </style>
</head>
<body>
  <div class="container">
    <header class="card">
      <div class="brand">
        <div class="logo">MW</div>
        <div>
          <div style="font-weight:700">Mi Web</div>
          <div class="muted" style="font-size:13px">Diseño moderno • Responsive</div>
        </div>
      </div>
      <nav>
        <a href="#">Inicio</a>
        <a href="#servicios">Servicios</a>
        <a href="#portafolio">Portafolio</a>
        <a href="#contacto">Contacto</a>
      </nav>
    </header>

    <section class="hero">
      <div class="card">
        <h1 class="title">Construyo sitios bonitos y rápidos</h1>
        <p class="lead">Plantilla lista para personalizar: portfolio, pequeña empresa o landing page. Incluye diseño oscuro, secciones reutilizables y formulario de contacto.</p>
        <a class="cta" href="#contacto">Contactarme</a>

        <div class="features" style="margin-top:18px">
          <div class="feature">
            <h4>Rápido</h4>
            <p>Carga ligera y estructura optimizada para buena performance.</p>
          </div>
          <div class="feature">
            <h4>Responsive</h4>
            <p>Se adapta a móviles, tablets y escritorios sin esfuerzo.</p>
          </div>
          <div class="feature">
            <h4>Editable</h4>
            <p>HTML, CSS y JS simple para que lo personalices a tu gusto.</p>
          </div>
        </div>
      </div>

      <aside class="mock card">
        <img src="data:image/svg+xml;utf8,<svg xmlns='http://www.w3.org/2000/svg' width='600' height='400'><rect fill='%230a1220' width='100%' height='100%'/><text x='50%' y='50%' fill='%23aab7c6' font-family='Arial' font-size='20' text-anchor='middle' dominant-baseline='middle'>Mockup de pantalla</text></svg>" alt="mockup">
        <p class="muted" style="margin-top:12px">Muestra de proyecto: reemplaza la imagen por tus capturas.</p>
      </aside>
    </section>

    <section id="servicios" class="grid-3">
      <div class="card">
        <h3>Diseño Web</h3>
        <p class="muted">UI/UX, wireframes y maquetado HTML/CSS.</p>
      </div>
      <div class="card">
        <h3>Desarrollo</h3>
        <p class="muted">JavaScript, interacción y pequeñas apps frontend.</p>
      </div>
      <div class="card">
        <h3>Optimización</h3>
        <p class="muted">Performance, accesibilidad y SEO técnico básico.</p>
      </div>
    </section>

    <section id="portafolio" class="card">
      <h2>Portafolio</h2>
      <p class="muted">Algunos trabajos recientes — haz clic para ver más.</p>
      <div style="display:grid;grid-template-columns:repeat(3,1fr);gap:12px;margin-top:12px">
        <div style="padding:10px;background:rgba(255,255,255,0.02);border-radius:10px">Proyecto A<br><span class="muted">Web corporativa</span></div>
        <div style="padding:10px;background:rgba(255,255,255,0.02);border-radius:10px">Proyecto B<br><span class="muted">Landing</span></div>
        <div style="padding:10px;background:rgba(255,255,255,0.02);border-radius:10px">Proyecto C<br><span class="muted">Tienda</span></div>
      </div>
    </section>

    <section id="contacto" class="card" style="margin-top:18px">
      <h2>Contacto</h2>
      <p class="muted">Escribe tus datos y un mensaje. (El formulario aquí es de ejemplo y no envía datos a un servidor).</p>
      <form id="contactForm" onsubmit="return handleSubmit(event)">
        <input id="name" placeholder="Tu nombre" required />
        <input id="email" type="email" placeholder="Tu correo" required />
        <textarea id="message" rows="5" placeholder="Tu mensaje"></textarea>
        <div style="display:flex;gap:12px;align-items:center">
          <button type="submit">Enviar mensaje</button>
          <div class="kbd">No enviará datos (demo)</div>
        </div>
      </form>
    </section>

    <footer>
      <div class="muted">© " + new Date().getFullYear() + " Mi Web • Hecho con cariño</div>
      <div class="muted">Sígueme en • Twitter • GitHub</div>
    </footer>
  </div>

  <script>
    // Función demo para evitar envío real
    function handleSubmit(e){
      e.preventDefault();
      const name=document.getElementById('name').value.trim();
      const email=document.getElementById('email').value.trim();
      const message=document.getElementById('message').value.trim();
      if(!name || !email){
        alert('Por favor completa nombre y correo.');
        return false;
      }
      alert('¡Gracias, ' + name + '! Tu mensaje ha sido capturado en demo.\n\nEmail: ' + email + '\nMensaje: ' + (message||'[sin mensaje]'));
      return false;
    }
  </script>
  <section>
    <h2>Cómo subir esta página a GitHub Pages</h2>
    <ol>
      <li>Asegúrate de haber guardado este archivo como <code>index.html</code>.</li>
      <li>Entra en tu repositorio de GitHub y ve a la pestaña <strong>Code</strong>.</li>
      <li>Haz clic en <strong>Add file</strong> → <strong>Upload files</strong>.</li>
      <li>Sube el archivo <code>index.html</code> y confirma con <strong>Commit changes</strong>.</li>
      <li>Ahora ve a <strong>Settings</strong> en la parte superior del repositorio.</li>
      <li>En el menú izquierdo baja hasta encontrar <strong>Pages</strong>.</li>
      <li>En la sección <strong>Build and deployment</strong>, selecciona:
        <ul>
          <li><strong>Source:</strong> Deploy from a branch</li>
          <li><strong>Branch:</strong> main / (root)</li>
        </ul>
      </li>
      <li>Guarda los cambios y espera unos 20–40 segundos.</li>
      <li>Aparecerá un mensaje con el enlace de tu página, normalmente algo como:<br>
        <code>https://tuusuario.github.io/tu-repo/</code>
      </li>
    </ol>
  </section>
</body>
</html>
