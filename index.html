<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Sensor IoT - Estación Meteorológica</title>
  <style>
    :root{
      --bg:#f4f7fb;
      --card:#ffffff;
      --text:#172033;
      --muted:#718096;
      --line:#e7ecf3;
      --primary:#0b3a70;
      --primary2:#2d6da8;
      --ok:#16a34a;
      --warn:#f59e0b;
      --danger:#dc2626;
      --shadow:0 10px 30px rgba(20,35,60,.08);
    }
    *{box-sizing:border-box}
    body{
      margin:0;
      font-family:Inter,Segoe UI,Arial,sans-serif;
      background:var(--bg);
      color:var(--text);
    }
    .top{
      background:linear-gradient(135deg,#061a2f,#0b3a70 65%,#14548a);
      color:white;
      padding:28px 5vw 34px;
    }
    .top-inner{
      max-width:1250px;
      margin:auto;
      display:flex;
      justify-content:space-between;
      align-items:center;
      gap:20px;
    }
    h1{margin:0;font-size:30px}
    .subtitle{margin:7px 0 0;color:#cbd5e1}
    .status{
      display:flex;align-items:center;gap:9px;
      background:rgba(255,255,255,.12);
      padding:10px 15px;border-radius:999px;
      font-size:14px;
    }
    .dot{width:10px;height:10px;border-radius:50%;background:#94a3b8}
    .dot.ok{background:#4ade80;box-shadow:0 0 12px #4ade80}
    .dot.bad{background:#fb7185}
    main{max-width:1250px;margin:-18px auto 40px;padding:0 20px}

    .flag{display:flex;width:72px;height:6px;margin-bottom:12px;border-radius:4px;overflow:hidden}
    .flag span:nth-child(1){flex:2;background:#f6d000}
    .flag span:nth-child(2){flex:1;background:#16479e}
    .flag span:nth-child(3){flex:1;background:#d91e2b}
    .mission-bar{
      background:#fff;border:1px solid var(--line);border-left:5px solid #0b3a70;
      border-radius:14px;padding:14px 18px;box-shadow:var(--shadow);
      display:flex;justify-content:space-between;align-items:center;gap:15px;margin-bottom:20px;
    }
    .institution{font-size:13px;font-weight:800;color:#0b3a70;letter-spacing:1px}
    .school{font-size:16px;font-weight:800;margin-top:3px;color:#172033}
    .project{font-size:11px;color:#718096;margin-top:4px;letter-spacing:.5px}
    .online{display:flex;align-items:center;gap:8px;font-size:13px;font-weight:700;white-space:nowrap}

    .config-unused{
      background:var(--card);border:1px solid var(--line);
      border-radius:16px;padding:15px 18px;box-shadow:var(--shadow);
      display:flex;gap:10px;align-items:center;margin-bottom:20px;
    }
    .config input{
      flex:1;min-width:0;border:1px solid #d8e0eb;border-radius:10px;
      padding:11px 12px;font-size:14px;outline:none;
    }
    button{
      border:0;border-radius:10px;padding:11px 16px;
      background:var(--primary);color:white;font-weight:600;cursor:pointer;
    }
    button:hover{filter:brightness(.96)}
    .grid{
      display:grid;grid-template-columns:repeat(4,1fr);gap:16px;
    }
    .card{
      background:var(--card);border:1px solid var(--line);
      border-radius:18px;padding:20px;box-shadow:var(--shadow);
      min-height:165px;
    }
    .label{color:var(--muted);font-size:14px;font-weight:600}
    .value{font-size:35px;font-weight:750;margin:16px 0 5px;letter-spacing:-1px}
    .unit{font-size:17px;color:var(--muted);font-weight:500}
    .pin{font-size:11px;color:#a0aec0}
    .icon{
      width:42px;height:42px;border-radius:12px;
      display:flex;align-items:center;justify-content:center;
      font-size:22px;background:#eff6ff;
    }
    .card-head{display:flex;justify-content:space-between;align-items:center}
    .light{
      margin-top:20px;
      display:inline-flex;align-items:center;gap:8px;
      padding:8px 12px;border-radius:999px;font-weight:700;font-size:14px;
      background:#ecfdf5;color:#15803d;
    }
    .light.dark{background:#fff7ed;color:#c2410c}
    .section-title{margin:30px 0 14px;font-size:20px}
    .charts{
      display:grid;grid-template-columns:repeat(2,1fr);gap:16px;
    }
    .chart-card{
      background:white;border:1px solid var(--line);border-radius:18px;
      padding:18px;box-shadow:var(--shadow);
    }
    canvas{width:100%;height:220px;display:block}
    .footer{
      text-align:center;color:var(--muted);font-size:13px;margin-top:25px;
    }
    .note{font-size:12px;color:var(--muted);margin:0 0 8px}
    @media(max-width:950px){.grid{grid-template-columns:repeat(2,1fr)}}
    @media(max-width:650px){
      .top-inner{align-items:flex-start;flex-direction:column}
      h1{font-size:25px}
      .grid,.charts{grid-template-columns:1fr}
  
    .flag{display:flex;width:72px;height:6px;margin-bottom:12px;border-radius:4px;overflow:hidden}
    .flag span:nth-child(1){flex:2;background:#f6d000}
    .flag span:nth-child(2){flex:1;background:#16479e}
    .flag span:nth-child(3){flex:1;background:#d91e2b}
    .mission-bar{
      background:#fff;border:1px solid var(--line);border-left:5px solid #0b3a70;
      border-radius:14px;padding:14px 18px;box-shadow:var(--shadow);
      display:flex;justify-content:space-between;align-items:center;gap:15px;margin-bottom:20px;
    }
    .institution{font-size:13px;font-weight:800;color:#0b3a70;letter-spacing:1px}
    .school{font-size:16px;font-weight:800;margin-top:3px;color:#172033}
    .project{font-size:11px;color:#718096;margin-top:4px;letter-spacing:.5px}
    .online{display:flex;align-items:center;gap:8px;font-size:13px;font-weight:700;white-space:nowrap}

    .config-unused{flex-direction:column;align-items:stretch}
      .config button{width:100%}
      main{padding:0 12px}
    }
  </style>
</head>
<body>

<header class="top">
  <div class="top-inner">
    <div>
      <div class="flag"><span></span><span></span><span></span></div>
      <h1>⚓ ESTACIÓN METEOROLÓGICA IoT</h1>
      <p class="subtitle">Sistema de monitoreo ambiental en tiempo real</p>
    </div>
  </div>
</header>

<main>
  <div class="mission-bar">
      <div>
        <div class="institution">⚓ ARMADA DEL ECUADOR</div>
        <div class="school">ESCUELA DE GRUMETES CONTRAMAESTRE JUAN SUÁREZ</div>
        <div class="project">ESTACIÓN METEOROLÓGICA IoT · PROYECTO ACADÉMICO</div>
      </div>
      <div class="online">
        <span id="statusDot" class="dot"></span>
        <span id="statusText">Conectando...</span>
      </div>
    </div>

    <section class="grid">
    <article class="card">
      <div class="card-head">
        <div class="label">Temperatura</div>
        <div class="icon">🌡️</div>
      </div>
      <div class="value"><span id="v0">--</span> <span class="unit">°C</span></div>
      <div class="pin">Blynk V0 · DHT22</div>
    </article>

    <article class="card">
      <div class="card-head">
        <div class="label">Humedad</div>
        <div class="icon">💧</div>
      </div>
      <div class="value"><span id="v1">--</span> <span class="unit">%</span></div>
      <div class="pin">Blynk V1 · DHT22</div>
    </article>

    <article class="card">
      <div class="card-head">
        <div class="label">Presión atmosférica</div>
        <div class="icon">🌬️</div>
      </div>
      <div class="value"><span id="v5">--</span> <span class="unit">hPa</span></div>
      <div class="pin">Blynk V5 · BME280</div>
    </article>

    <article class="card">
      <div class="card-head">
        <div class="label">Altitud</div>
        <div class="icon">⛰️</div>
      </div>
      <div class="value"><span id="v6">--</span> <span class="unit">m</span></div>
      <div class="pin">Blynk V6 · BME280</div>
    </article>

    <article class="card">
      <div class="card-head">
        <div class="label">Distancia</div>
        <div class="icon">📏</div>
      </div>
      <div class="value"><span id="v2">--</span> <span class="unit">cm</span></div>
      <div class="pin">Blynk V2 · HC-SR04</div>
    </article>

    <article class="card">
      <div class="card-head">
        <div class="label">Luminosidad</div>
        <div class="icon">☀️</div>
      </div>
      <div id="lightState" class="light">Esperando dato...</div>
      <div class="pin" style="margin-top:12px">Blynk V7 · LDR digital</div>
    </article>

    <article class="card">
      <div class="card-head">
        <div class="label">Actualización</div>
        <div class="icon">🕐</div>
      </div>
      <div class="value" style="font-size:25px" id="lastUpdate">--:--:--</div>
      <div class="pin">Lectura de Blynk Cloud</div>
    </article>

    <article class="card">
      <div class="card-head">
        <div class="label">Estado del sistema</div>
        <div class="icon">📡</div>
      </div>
      <div class="value" style="font-size:24px" id="systemState">Desconectado</div>
      <div class="pin">Consulta automática cada 2 segundos</div>
    </article>
  </section>

  <h2 class="section-title">📊 Historial de lecturas</h2>
  <section class="charts">
    <div class="chart-card">
      <strong>Temperatura</strong>
      <canvas id="tempChart"></canvas>
    </div>
    <div class="chart-card">
      <strong>Humedad</strong>
      <canvas id="humChart"></canvas>
    </div>
  </section>

  <p class="footer">
    ESP32 → Blynk Cloud → Dashboard web · Los datos se actualizan automáticamente.
  </p>
</main>

<script>
  const API = "https://blynk.cloud/external/api/getAll";
  let token = "NOFYjv5bXJJN8QnVuskfEms6bMj55tgb";
  let timer = null;
  const history = {temp:[], hum:[], labels:[]};
  const MAX_POINTS = 30;

  function conectar(){
    token = "NOFYjv5bXJJN8QnVuskfEms6bMj55tgb";
    if(timer) clearInterval(timer);
    leerBlynk();
    timer = setInterval(leerBlynk, 2000);
  }

  async function leerBlynk(){
    if(!token) return;

    try{
      const respuesta = await fetch(API + "?token=" + encodeURIComponent(token) + "&_=" + Date.now(), {
        cache: "no-store"
      });

      if(!respuesta.ok) throw new Error("HTTP " + respuesta.status);

      const datos = await respuesta.json();

      // Blynk devuelve los virtual pins como v0, v1, v2...
      const temp = numero(datos.v0);
      const hum  = numero(datos.v1);
      const dist = numero(datos.v2);
      const pres = numero(datos.v5);
      const alt  = numero(datos.v6);
      const ldr  = numero(datos.v7);

      mostrar("v0", temp, 1);
      mostrar("v1", hum, 1);
      mostrar("v2", dist, 1);
      mostrar("v5", pres, 1);
      mostrar("v6", alt, 1);

      if(ldr !== null){
        const estado = document.getElementById("lightState");
        if(ldr === 0){
          estado.textContent = "☀️ Hay luz";
          estado.className = "light";
        }else{
          estado.textContent = "🌙 Poca luz";
          estado.className = "light dark";
        }
      }

      const ahora = new Date();
      document.getElementById("lastUpdate").textContent =
        ahora.toLocaleTimeString("es-EC");
      document.getElementById("systemState").textContent = "Conectado";

      document.getElementById("statusDot").className = "dot ok";
      document.getElementById("statusText").textContent = "Blynk conectado";

      if(temp !== null && hum !== null){
        history.temp.push(temp);
        history.hum.push(hum);
        history.labels.push(ahora.toLocaleTimeString("es-EC",{hour:"2-digit",minute:"2-digit",second:"2-digit"}));

        if(history.temp.length > MAX_POINTS){
          history.temp.shift();
          history.hum.shift();
          history.labels.shift();
        }
        dibujarGrafica("tempChart", history.temp, history.labels, "°C");
        dibujarGrafica("humChart", history.hum, history.labels, "%");
      }

    }catch(error){
      document.getElementById("statusDot").className = "dot bad";
      document.getElementById("statusText").textContent = "Sin respuesta";
      document.getElementById("systemState").textContent = "Error de conexión";
      console.error(error);
    }
  }

  function numero(x){
    if(x === undefined || x === null || x === "") return null;
    const n = Number(x);
    return Number.isFinite(n) ? n : null;
  }

  function mostrar(id, valor, decimales){
    document.getElementById(id).textContent =
      valor === null ? "--" : valor.toFixed(decimales);
  }

  function dibujarGrafica(id, valores, etiquetas, unidad){
    const canvas = document.getElementById(id);
    const ctx = canvas.getContext("2d");
    const w = canvas.width = canvas.clientWidth * devicePixelRatio;
    const h = canvas.height = canvas.clientHeight * devicePixelRatio;
    ctx.scale(devicePixelRatio, devicePixelRatio);

    const W = canvas.clientWidth;
    const H = canvas.clientHeight;

    ctx.clearRect(0,0,W,H);

    if(valores.length < 2) return;

    const pad = {l:42,r:12,t:20,b:30};
    const pw = W-pad.l-pad.r;
    const ph = H-pad.t-pad.b;

    let min = Math.min(...valores);
    let max = Math.max(...valores);
    if(min === max){ min -= 1; max += 1; }
    const extra = (max-min)*0.15;
    min -= extra; max += extra;

    ctx.font = "11px Segoe UI, Arial";
    ctx.strokeStyle = "#e8edf4";
    ctx.lineWidth = 1;

    for(let i=0;i<5;i++){
      const y = pad.t + ph*i/4;
      ctx.beginPath(); ctx.moveTo(pad.l,y); ctx.lineTo(W-pad.r,y); ctx.stroke();
      const val = max - (max-min)*i/4;
      ctx.fillStyle = "#718096";
      ctx.fillText(val.toFixed(1)+" "+unidad, 4, y+4);
    }

    ctx.beginPath();
    valores.forEach((v,i)=>{
      const x = pad.l + (pw*i/(valores.length-1));
      const y = pad.t + ph*(1-(v-min)/(max-min));
      if(i===0) ctx.moveTo(x,y); else ctx.lineTo(x,y);
    });
    ctx.strokeStyle = "#2563eb";
    ctx.lineWidth = 3;
    ctx.stroke();

    valores.forEach((v,i)=>{
      const x = pad.l + (pw*i/(valores.length-1));
      const y = pad.t + ph*(1-(v-min)/(max-min));
      ctx.beginPath();
      ctx.arc(x,y,3.5,0,Math.PI*2);
      ctx.fillStyle = "#2563eb";
      ctx.fill();
    });

    ctx.fillStyle = "#718096";
    if(etiquetas.length){
      ctx.fillText(etiquetas[0], pad.l, H-8);
      const last = etiquetas[etiquetas.length-1];
      ctx.fillText(last, W-pad.r-55, H-8);
    }
  }

  window.addEventListener("load", conectar);

  window.addEventListener("resize", ()=>{
    if(history.temp.length > 1){
      dibujarGrafica("tempChart", history.temp, history.labels, "°C");
      dibujarGrafica("humChart", history.hum, history.labels, "%");
    }
  });
</script>
</body>
</html>
