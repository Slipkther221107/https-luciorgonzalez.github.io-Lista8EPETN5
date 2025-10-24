# https-luciorgonzalez.github.io-Lista8EPETN5
<!doctype html>
<html lang="es">
<head>
  <meta charset="utf-8" />
  <meta name="viewport" content="width=device-width,initial-scale=1" />
  <title>Lista Azul N°8 — Centro de Estudiantes</title>
  <link href="https://fonts.googleapis.com/css2?family=Poppins:wght@300;400;600;700&display=swap" rel="stylesheet">
  <style>
    :root{
      --navy:#062130; /* azul marino profundo */
      --accent:#1E88E5; /* azul brillante */
      --muted:#9aa7b2; /* gris claro */
      --card:#0b2a3f; /* tarjeta oscuro */
      --glass: rgba(255,255,255,0.04);
      --glass-2: rgba(255,255,255,0.03);
      --white-90: rgba(255,255,255,0.95);
    }
    *{box-sizing:border-box}
    html,body{height:100%;margin:0;font-family:Poppins,system-ui,Arial; background:linear-gradient(180deg,var(--navy),#031726);color:var(--white-90)}
    a{color:inherit;text-decoration:none}
    .container{max-width:1100px;margin:0 auto;padding:28px}

    /* Navbar */
    header{position:sticky;top:12px;z-index:50}
    .nav{display:flex;align-items:center;justify-content:space-between;padding:10px 14px;border-radius:12px;background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));backdrop-filter: blur(6px);box-shadow:0 6px 18px rgba(2,6,23,0.45)}
    .brand{display:flex;gap:12px;align-items:center}
    .logo{width:56px;height:56px;border-radius:10px;background:linear-gradient(135deg,var(--accent),#0bb0ff);display:flex;align-items:center;justify-content:center;font-weight:700;color:#042135}
    .brand h1{font-size:18px;margin:0}
    .brand p{margin:0;font-size:12px;color:var(--muted)}
    .nav-links{display:flex;gap:10px}
    .btn{padding:8px 14px;border-radius:10px;font-weight:600;background:transparent;border:1px solid rgba(255,255,255,0.06);cursor:pointer}
    .btn-primary{background:linear-gradient(90deg,var(--accent),#0bb0ff);color:#042135;border:0}

    /* Hero */
    .hero{display:grid;grid-template-columns:1fr 420px;gap:28px;align-items:center;padding:48px 0}
    .hero-card{background:linear-gradient(180deg,var(--glass),var(--glass-2));padding:28px;border-radius:14px;border:1px solid rgba(255,255,255,0.03);box-shadow:0 8px 30px rgba(1,6,20,0.5)}
    .hero h2{margin:0;font-size:28px}
    .hero p{color:var(--muted);line-height:1.5}
    .cta{display:flex;gap:12px;margin-top:18px}

    /* Hero right */
    .card-stats{padding:20px;border-radius:12px;background:linear-gradient(180deg,#0a2a3f, #042135);border:1px solid rgba(255,255,255,0.03)}
    .highlight{font-size:34px;font-weight:700}
    .sub{color:var(--muted);font-size:13px}

    /* Proposals */
    section{padding:48px 0}
    .grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:16px}
    .proposal{background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));padding:18px;border-radius:10px;border:1px solid rgba(255,255,255,0.03);min-height:80px}
    .proposal h4{margin:0 0 8px 0}
    .icon{width:40px;height:40px;border-radius:8px;display:inline-grid;place-items:center;margin-right:10px;background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));border:1px solid rgba(255,255,255,0.04)}

    /* Team */
    .team-grid{display:grid;grid-template-columns:repeat(auto-fit,minmax(160px,1fr));gap:14px}
    .member{background:linear-gradient(180deg, rgba(255,255,255,0.02), rgba(255,255,255,0.01));padding:12px;border-radius:10px;display:flex;gap:12px;align-items:center}
    .avatar{width:56px;height:56px;border-radius:10px;background:linear-gradient(135deg,var(--accent),#0bb0ff);display:flex;align-items:center;justify-content:center;font-weight:700;color:#042135}
    .role{color:var(--muted);font-size:13px}

    footer{padding:36px 0;text-align:center}
    .slogan{font-weight:700;font-size:20px;padding:28px;border-radius:12px;background:linear-gradient(90deg,var(--accent),#0bb0ff);display:inline-block;color:#042135}

    /* Small screens */
    @media (max-width:900px){
      .hero{grid-template-columns:1fr;}
      .nav{flex-direction:column;gap:10px}
      .brand h1{font-size:16px}
    }

    /* subtle animated lines (technical touch) */
    .tech-lines{position:absolute;inset:0;pointer-events:none;opacity:0.06}
    .tech-lines svg{width:100%;height:100%}

    /* smooth appear */
    .reveal{opacity:0;transform:translateY(12px);transition:all 600ms cubic-bezier(.2,.9,.3,1)}
    .reveal.visible{opacity:1;transform:none}
  </style>
</head>
<body>
  <div class="tech-lines" aria-hidden>
    <svg viewBox="0 0 1200 600" preserveAspectRatio="none">
      <g stroke="white" stroke-width="0.5" fill="none">
        <path d="M0 520 C300 430 900 600 1200 480" opacity="0.08"></path>
        <path d="M0 380 C200 300 1000 420 1200 350" opacity="0.06"></path>
      </g>
    </svg>
  </div>

  <div class="container">
    <header>
      <nav class="nav">
        <div class="brand">
          <div class="logo">A8</div>
          <div>
            <h1>Lista Azul N°8</h1>
            <p>Centro de Estudiantes — E.P.E.T. N°5</p>
          </div>
        </div>
        <div class="nav-links">
          <button class="btn" onclick="scrollToId('inicio')">Inicio</button>
          <button class="btn" onclick="scrollToId('propuestas')">Propuestas</button>
          <button class="btn" onclick="scrollToId('equipo')">Equipo</button>
          <a class="btn btn-primary" href="#final">Votar / Contacto</a>
        </div>
      </nav>
    </header>

    <!-- HERO / INICIO -->
    <main id="inicio" class="hero">
      <div class="hero-card reveal">
        <h2>¡Bienvenidos a la Lista Azul N°8!</h2>
        <p>Somos estudiantes con una meta clara: <strong>mejorar nuestra escuela desde adentro, con ideas reales y acción técnica</strong>. Este sitio presenta nuestras propuestas pensadas por y para los estudiantes, con una mirada innovadora, responsable y comprometida con nuestra formación técnica.</p>
        <div class="cta">
          <button class="btn btn-primary" onclick="scrollToId('propuestas')">Ver propuestas</button>
          <button class="btn" onclick="scrollToId('equipo')">Conocer al equipo</button>
        </div>

        <hr style="margin:18px 0;border:0;border-top:1px solid rgba(255,255,255,0.03)">
        <p style="color:var(--muted);font-size:14px">Alumnos, docentes, preceptores y directivos: los invitamos a conocer nuestro trabajo, a sumar sus ideas y a ser parte del cambio que soñamos para nuestra comunidad educativa.</p>
      </div>

      <aside class="card-stats reveal">
        <div style="display:flex;align-items:center;justify-content:space-between">
          <div>
            <div class="sub">Lista</div>
            <div class="highlight">Azul N°8</div>
          </div>
          <div style="text-align:right">
            <div class="sub">Escuela</div>
            <div style="font-weight:600">E.P.E.T. N°5</div>
          </div>
        </div>
        <div style="margin-top:16px;color:var(--muted);font-size:13px">"Técnicos en acción, líderes en transformación."</div>
      </aside>
    </main>

    <!-- PROPUESTAS -->
    <section id="propuestas" class="reveal">
      <div style="display:flex;justify-content:space-between;align-items:center;margin-bottom:18px">
        <h3>Propuestas</h3>
        <p style="color:var(--muted);margin:0">Ideas pensadas para mejorar la vida escolar, técnicas y prácticas.</p>
      </div>

      <div class="grid">
        <!-- Proposals inserted from user file -->
        <div class="proposal"><h4>Mejor ventilación</h4><p class="role">Mejor ventilación para los baños de la escuela y taller.</p></div>
        <div class="proposal"><h4>Eventos recreativos</h4><p class="role">Realización de eventos recreativos.</p></div>
        <div class="proposal"><h4>Charlas informativas</h4><p class="role">Charlas informativas de ESI, bullying, seguridad vial, etc.</p></div>
        <div class="proposal"><h4>Botiquines</h4><p class="role">Botiquines de primeros auxilios en cada curso y taller.</p></div>
        <div class="proposal"><h4>Renovación de pizarrones</h4><p class="role">Renovación de pizarrones.</p></div>
        <div class="proposal"><h4>Accesibilidad</h4><p class="role">Habilitación de una habitación en óptimas condiciones para alumnos con problemas de movilidad.</p></div>
        <div class="proposal"><h4>Enfermería</h4><p class="role">Enfermería.</p></div>
        <div class="proposal"><h4>Pupitres</h4><p class="role">Adquisición y reparación de nuevos pupitres (sillas y mesas).</p></div>
        <div class="proposal"><h4>Buzón anónimo</h4><p class="role">Buzón de quejas de alumnos (anónimo).</p></div>
        <div class="proposal"><h4>Charlas sobre universidades</h4><p class="role">Charlas y concientización sobre universidades.</p></div>
        <div class="proposal"><h4>Buzón de sugerencias</h4><p class="role">Buzón de sugerencias.</p></div>
        <div class="proposal"><h4>Higiene</h4><p class="role">Cajón de elementos higiénicos (papel higiénico, toallitas, etc.).</p></div>
        <div class="proposal"><h4>Dispensadores</h4><p class="role">Colocación de dispensadores de jabón, alcohol, y perfume en los baños.</p></div>
        <div class="proposal"><h4>Portarrollos</h4><p class="role">Portarrollos de papel en los baños.</p></div>
        <div class="proposal"><h4>Bancos plegables</h4><p class="role">Colocación de bancos plegables en las paredes de la institución.</p></div>
        <div class="proposal"><h4>Luminarias</h4><p class="role">Agregado de luminarias en el interior y exterior en la escuela.</p></div>
        <div class="proposal"><h4>Juegos didácticos</h4><p class="role">Adquisición de nuevos juegos didácticos para el horario libre.</p></div>
        <div class="proposal"><h4>Mobiliario de entrada</h4><p class="role">Agregar más sillones y mesas ratoneras en la entrada y en el SUM.</p></div>
        <div class="proposal"><h4>Basureros</h4><p class="role">Basureros nuevos, tanto orgánicos e inorgánicos en las aulas.</p></div>
        <div class="proposal"><h4>Elementos deportivos</h4><p class="role">Nuevos elementos deportivos.</p></div>
        <div class="proposal"><h4>Tomacorrientes y ventiladores</h4><p class="role">Reparación y colocación de tomacorrientes y ventiladores.</p></div>
        <div class="proposal"><h4>Separador de urinarios</h4><p class="role">Separador de urinarios.</p></div>
        <div class="proposal"><h4>Dispensadores de agua</h4><p class="role">Reparación de dispensadores de agua.</p></div>
        <div class="proposal"><h4>Casilleros</h4><p class="role">Casilleros para guardar objetos personales.</p></div>
        <div class="proposal"><h4>Biblioteca en entrada</h4><p class="role">Disponibilidad de libros en la entrada.</p></div>
        <div class="proposal"><h4>Remodelación</h4><p class="role">Remodelación de espacios sin utilidad.</p></div>
      </div>
    </section>

    <!-- EQUIPO -->
    <section id="equipo" class="reveal">
      <div style="display:flex;justify-content:space-between;align-items:center;margin-bottom:18px">
        <h3>Equipo</h3>
        <p style="color:var(--muted);margin:0">Integrantes de la Lista Azul N°8</p>
      </div>

      <div class="team-grid">
        <!-- Using names from the uploaded file -->
        <div class="member"><div class="avatar">LG</div><div><div style="font-weight:600">Presidente: González Lucio</div><div class="role">Presidente</div></div></div>
        <div class="member"><div class="avatar">—</div><div><div style="font-weight:600">Vicepresidente: (vacante)</div><div class="role">Vicepresidente</div></div></div>
        <div class="member"><div class="avatar">MA</div><div><div style="font-weight:600">Secretario General: Montenegro Aldana</div><div class="role">Secretario General</div></div></div>
        <div class="member"><div class="avatar">AJ</div><div><div style="font-weight:600">Pro - Secretario General: Alvarenga Johana</div><div class="role">Pro - Secretario General</div></div></div>
        <div class="member"><div class="avatar">NR</div><div><div style="font-weight:600">Tesorero: Rodríguez Nicolás</div><div class="role">Tesorero</div></div></div>
        <div class="member"><div class="avatar">SR</div><div><div style="font-weight:600">Pro - Tesorero: Rojas Santiago</div><div class="role">Pro - Tesorero</div></div></div>
        <div class="member"><div class="avatar">JO</div><div><div style="font-weight:600">Secretario de Taller: Ojeda Juan</div><div class="role">Secretario de Taller</div></div></div>
        <div class="member"><div class="avatar">EG</div><div><div style="font-weight:600">Pro – Secretario de Taller: Gareca Elías</div><div class="role">Pro - Secretario de Taller</div></div></div>
        <div class="member"><div class="avatar">LB</div><div><div style="font-weight:600">Secretario de Relaciones Públicas: Benitez Lucía</div><div class="role">Relaciones Públicas</div></div></div>
        <div class="member"><div class="avatar">FY</div><div><div style="font-weight:600">Secretario de Deportes: Yakowecz Felipe</div><div class="role">Deportes</div></div></div>
        <div class="member"><div class="avatar">CA</div><div><div style="font-weight:600">Secretario de Eventos: Caballero Agustina</div><div class="role">Eventos</div></div></div>
        <div class="member"><div class="avatar">AL</div><div><div style="font-weight:600">Secretario de Sanidad y Cuidados: Lezcano Agustín</div><div class="role">Sanidad</div></div></div>
        <div class="member"><div class="avatar">CM</div><div><div style="font-weight:600">Pro – Secretario de Sanidad y Cuidados: Melo Carla</div><div class="role">Pro - Sanidad</div></div></div>
      </div>

      <p style="color:var(--muted);font-size:13px;margin-top:12px">(Aquí podrán agregarse las fotos más adelante. Para reemplazar, suban imágenes y pongan la ruta en el elemento .avatar)</p>
    </section>

    <!-- FINAL -->
    <section id="final" class="reveal" style="padding-top:36px">
      <div style="display:flex;flex-direction:column;align-items:center;gap:14px">
        <div class="slogan">Técnicos en acción, líderes en transformación.</div>
        <p style="color:var(--muted);max-width:760px">Si querés contactarnos o sugerir alguna mejora: <strong>Email:</strong> listaazul8@example.com • <strong>QR:</strong> (pega aquí tu enlace) • <strong>Teléfono/WhatsApp:</strong> (opcional)</p>
        <small style="color:var(--muted)">Gracias por leer nuestras propuestas — tu apoyo y tu voto hacen la diferencia.</small>
      </div>
    </section>

    <footer>
      <small style="color:var(--muted)">Diseño por Lista Azul N°8 • E.P.E.T. N°5</small>
    </footer>
  </div>

  <script>
    // Simple scroll + reveal logic
    function scrollToId(id){
      const el = document.getElementById(id);
      if(!el) return;
      el.scrollIntoView({behavior:'smooth',block:'start'});
    }

    // Reveal on scroll
    const reveals = document.querySelectorAll('.reveal');
    const obs = new IntersectionObserver((entries)=>{
      entries.forEach(e=>{
        if(e.isIntersecting){
          e.target.classList.add('visible');
        }
      });
    },{threshold:0.12});
    reveals.forEach(r=>obs.observe(r));
  </script>
</body>
</html>
