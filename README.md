<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1">
<title>NexusMzStudioVLS · Launchers</title>
<link href="https://fonts.googleapis.com/css2?family=Orbitron:wght@600;800&family=Nunito:wght@400;600&display=swap" rel="stylesheet">
<style>
  :root{
    --bg:#0a0818; --panel:#15112b; --line:#2c2455;
    --text:#e9e6ff; --muted:#a29cc9;
    --violet:#8b5cf6; --cyan:#22d3ee; --pink:#f472b6;
    color-scheme: dark;
  }
  *{box-sizing:border-box;margin:0}
  html{scroll-behavior:smooth}
  body{
    background:var(--bg); color:var(--text);
    font-family:'Nunito',system-ui,sans-serif; line-height:1.65;
    min-height:100vh; overflow-x:hidden;
  }
  #net{position:fixed;inset:0;width:100%;height:100%;z-index:0}
  main{position:relative;z-index:1;max-width:860px;margin:0 auto;padding:72px 22px 48px}

  /* Hero */
  .hero{text-align:center;padding:30px 0 56px}
  .logo{
    width:92px;height:92px;margin:0 auto 26px;border-radius:26px;
    display:grid;place-items:center;
    font:800 40px 'Orbitron',sans-serif;
    background:linear-gradient(135deg,var(--violet),var(--cyan));
    box-shadow:0 0 40px rgba(139,92,246,.55);
    animation:float 4s ease-in-out infinite, glow 3s ease-in-out infinite;
  }
  @keyframes float{50%{transform:translateY(-10px) rotate(3deg)}}
  @keyframes glow{50%{box-shadow:0 0 70px rgba(34,211,238,.6)}}

  h1{
    font:800 clamp(28px,6vw,52px)/1.15 'Orbitron',sans-serif;
    background:linear-gradient(90deg,var(--cyan),var(--violet),var(--pink),var(--cyan));
    background-size:300% 100%;
    -webkit-background-clip:text;background-clip:text;color:transparent;
    animation:shine 6s linear infinite;
  }
  @keyframes shine{to{background-position:300% 0}}
  .welcome{margin-top:18px;font-size:1.2rem;color:var(--muted)}
  .typed{
    display:inline-block;border-right:2px solid var(--cyan);
    padding-right:4px;animation:blink .8s step-end infinite;
  }
  @keyframes blink{50%{border-color:transparent}}

  /* Secciones */
  section{
    background:linear-gradient(160deg,rgba(21,17,43,.92),rgba(14,11,31,.92));
    border:1px solid var(--line);border-radius:22px;
    padding:34px 30px;margin-top:26px;
    backdrop-filter:blur(6px);
  }
  h2{font:600 1.35rem 'Orbitron',sans-serif;margin-bottom:8px}
  .sub{color:var(--muted);margin-bottom:24px}

  /* Botones de contacto */
  .links{display:grid;grid-template-columns:repeat(auto-fit,minmax(220px,1fr));gap:16px}
  .btn{
    display:flex;align-items:center;gap:14px;padding:16px 18px;
    border-radius:16px;text-decoration:none;color:#fff;font-weight:600;
    border:1px solid transparent;
    transition:transform .2s, box-shadow .2s;
  }
  .btn svg{width:28px;height:28px;flex:none;fill:currentColor}
  .btn small{display:block;font-weight:400;opacity:.8;font-size:.8rem}
  .btn:hover,.btn:focus-visible{transform:translateY(-4px) scale(1.02);outline:none}
  .discord{background:#5865f2}.discord:hover,.discord:focus-visible{box-shadow:0 10px 30px rgba(88,101,242,.55)}
  .web{background:linear-gradient(135deg,var(--violet),#6d28d9)}.web:hover,.web:focus-visible{box-shadow:0 10px 30px rgba(139,92,246,.55)}
  .facebook{background:#1877f2}.facebook:hover,.facebook:focus-visible{box-shadow:0 10px 30px rgba(24,119,242,.55)}

  /* Términos */
  ol{list-style:none;counter-reset:t;display:grid;gap:16px}
  ol li{
    counter-increment:t;position:relative;
    padding:18px 20px 18px 62px;border-radius:14px;
    background:rgba(139,92,246,.07);border:1px solid var(--line);
  }
  ol li::before{
    content:counter(t);position:absolute;left:16px;top:16px;
    width:32px;height:32px;border-radius:10px;display:grid;place-items:center;
    font:600 .95rem 'Orbitron',sans-serif;
    background:linear-gradient(135deg,var(--violet),var(--cyan));
  }
  ol li strong{display:block;margin-bottom:4px;color:var(--cyan)}
  .warden{color:var(--pink);font-family:'Orbitron',sans-serif;font-size:.9em}

  footer{text-align:center;margin-top:40px;color:var(--muted);font-size:.9rem}

  @media (prefers-reduced-motion:reduce){
    *{animation:none!important;transition:none!important}
    html{scroll-behavior:auto}
  }
</style>
</head>
<body>
<canvas id="net" aria-hidden="true"></canvas>

<main>
  <header class="hero">
    <div class="logo" aria-hidden="true">N</div>
    <h1>NexusMzStudioVLS</h1>
    <p class="welcome"><span class="typed" id="typed"></span></p>
  </header>

  <section id="contacto">
    <h2>¿Deseas adquirir algún producto con nosotros?</h2>
    <p class="sub">Contáctanos por cualquiera de estos medios:</p>
    <div class="links">
      <!-- Reemplaza cada "#" por tu enlace real -->
      <a class="btn discord" href="#" target="_blank" rel="noopener">
        <svg viewBox="0 0 24 24"><path d="M20.3 4.4A19.8 19.8 0 0 0 15.4 3l-.2.4a18 18 0 0 1 4.3 1.4 14.7 14.7 0 0 0-15 0A18 18 0 0 1 8.8 3.4L8.6 3a19.8 19.8 0 0 0-4.9 1.5C.6 9.100 0 13.600.3 18.100a19.9 19.900 0 0 0 6 3l1.300-2.100a13 13 0 0 1-2-1l.5-.4a14.200 14.200 0 0 0 12.100 0l.5.4a13 13 0 0 1-2 1l1.300 2.100a19.900 19.900 0 0 0 6-3c.5-5.200-.8-9.700-3.700-13.700ZM8.500 15.300c-1.200 0-2.100-1.100-2.100-2.400s.9-2.400 2.100-2.400 2.100 1.100 2.100 2.400-.9 2.400-2.100 2.400Zm7 0c-1.200 0-2.100-1.100-2.100-2.400s.9-2.400 2.100-2.400 2.100 1.100 2.100 2.400-.9 2.400-2.100 2.400Z"/></svg>
        <span>Discord<small>Únete a la comunidad</small></span>
      </a>
      <a class="btn web" href="#" target="_blank" rel="noopener">
        <svg viewBox="0 0 24 24"><path d="M12 2a10 10 0 1 0 0 20 10 10 0 0 0 0-20Zm6.900 9h-3a15.600 15.600 0 0 0-1.300-5.300A8 8 0 0 1 18.900 11ZM12 4c.8 1 1.700 3 2 7H10c.3-4 1.200-6 2-7ZM9.400 5.700A15.600 15.600 0 0 0 8.100 11h-3a8 8 0 0 1 4.300-5.300ZM5.100 13h3a15.600 15.600 0 0 0 1.300 5.300A8 8 0 0 1 5.100 13ZM12 20c-.8-1-1.700-3-2-7h4c-.3 4-1.200 6-2 7Zm2.600-1.700a15.600 15.600 0 0 0 1.300-5.300h3a8 8 0 0 1-4.300 5.300Z"/></svg>
        <span>Página web<small>Conoce nuestros productos</small></span>
      </a>
      <a class="btn facebook" href="#" target="_blank" rel="noopener">
        <svg viewBox="0 0 24 24"><path d="M22 12a10 10 0 1 0-11.600 9.900v-7H7.900V12h2.500V9.800c0-2.500 1.500-3.900 3.800-3.900 1.100 0 2.200.2 2.200.2v2.500h-1.300c-1.200 0-1.600.8-1.600 1.600V12h2.800l-.4 2.900h-2.300v7A10 10 0 0 0 22 12Z"/></svg>
        <span>Facebook<small>Novedades y anuncios</small></span>
      </a>
    </div>
  </section>

  <section id="terminos">
    <h2>Términos &amp; Condiciones</h2>
    <p class="sub">Al usar nuestros productos aceptas lo siguiente:</p>
    <ol>
      <li>
        <strong>Antivirus</strong>
        Debes quitar o desactivar el antivirus (o, como mínimo, agregar la carpeta del launcher a las exclusiones) para que el programa funcione correctamente.
      </li>
      <li>
        <strong>Seguridad y falsos positivos</strong>
        Nuestro programa no contiene virus ni ningún sistema que vulnere tu equipo o recolecte información personal. Debido a nuestro sistema <span class="warden">WARDEN</span>, cualquier antivirus puede detectar un falso positivo: es la protección que resguarda nuestro sistema y evita manipulaciones.
      </li>
      <li>
        <strong>Revisión de código</strong>
        Si eres propietario de algún launcher o sistema, puedes hablar con el dueño de NexusMzStudio y solicitar una revisión breve de nuestro código privado.
      </li>
    </ol>
  </section>

  <footer>© NexusMzStudioVLS · Todos los derechos reservados</footer>
</main>

<script>
  // Texto con efecto de escritura
  (function(){
    var text = "Hola, bienvenido al Repositorio para los Launcher de NexusMzStudioVLS";
    var el = document.getElementById('typed');
    if (matchMedia('(prefers-reduced-motion: reduce)').matches) { el.textContent = text; return; }
    var i = 0;
    (function type(){
      el.textContent = text.slice(0, ++i);
      if (i < text.length) setTimeout(type, 45);
    })();
  })();

  // Fondo animado: red de nodos
  (function(){
    if (matchMedia('(prefers-reduced-motion: reduce)').matches) return;
    var c = document.getElementById('net'), x = c.getContext('2d'), pts = [], W, H;
    function size(){
      W = c.width = innerWidth; H = c.height = innerHeight;
      var n = Math.min(80, Math.floor(W * H / 16000));
      pts = [];
      for (var i = 0; i < n; i++) pts.push({
        x: Math.random()*W, y: Math.random()*H,
        vx: (Math.random()-.5)*.5, vy: (Math.random()-.5)*.5
      });
    }
    function draw(){
      x.clearRect(0,0,W,H);
      for (var i = 0; i < pts.length; i++){
        var p = pts[i];
        p.x += p.vx; p.y += p.vy;
        if (p.x < 0 || p.x > W) p.vx *= -1;
        if (p.y < 0 || p.y > H) p.vy *= -1;
        x.fillStyle = 'rgba(139,92,246,.8)';
        x.beginPath(); x.arc(p.x, p.y, 1.8, 0, 6.283); x.fill();
        for (var j = i+1; j < pts.length; j++){
          var q = pts[j], dx = p.x-q.x, dy = p.y-q.y, d = Math.sqrt(dx*dx+dy*dy);
          if (d < 140){
            x.strokeStyle = 'rgba(34,211,238,' + (1 - d/140)*.35 + ')';
            x.beginPath(); x.moveTo(p.x,p.y); x.lineTo(q.x,q.y); x.stroke();
          }
        }
      }
      requestAnimationFrame(draw);
    }
    addEventListener('resize', size);
    size(); draw();
  })();
</script>
</body>
</html>
