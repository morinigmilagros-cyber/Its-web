<!DOCTYPE html>
<html lang="es">
<head>
  <meta charset="UTF-8">
  <meta name="viewport" content="width=device-width, initial-scale=1.0">
  <title>Prevenir es cuidar: ITS y salud sexual</title>
  <link href="https://fonts.googleapis.com/css2?family=Roboto:wght@400;700&display=swap" rel="stylesheet">
  <style>
    body {
      margin: 0;
      font-family: 'Roboto', sans-serif;
      background-color: #ffffff;
      color: #333;
      scroll-behavior: smooth;
    }

    /* Header y navegación */
    header {
      background: linear-gradient(90deg, #1E90FF, #DA70D6);
      color: white;
      padding: 20px 0;
      text-align: center;
      position: sticky;
      top: 0;
      z-index: 1000;
      box-shadow: 0 4px 6px rgba(0,0,0,0.1);
    }
    nav a {
      color: white;
      margin: 0 20px;
      text-decoration: none;
      font-weight: bold;
      transition: color 0.3s;
    }
    nav a:hover {
      color: #FFD700;
    }

    section {
      padding: 80px 20px;
      max-width: 900px;
      margin: auto;
    }

    h2 {
      color: #1E90FF;
      border-bottom: 3px solid #DA70D6;
      display: inline-block;
      padding-bottom: 5px;
    }

    .card {
      background-color: #f0f8ff;
      border-left: 5px solid #DA70D6;
      padding: 20px;
      margin: 20px 0;
      border-radius: 10px;
      box-shadow: 0 4px 8px rgba(0,0,0,0.05);
      transition: transform 0.3s;
    }
    .card:hover {
      transform: translateY(-5px);
    }

    /* Formulario encuesta */
    form {
      background-color: #f9f9ff;
      padding: 25px;
      border-radius: 12px;
      border: 2px solid #DA70D6;
      box-shadow: 0 4px 8px rgba(0,0,0,0.1);
    }
    label {
      display: block;
      margin: 15px 0 5px;
      font-weight: 500;
    }
    input[type="radio"] {
      margin-right: 10px;
    }
    button {
      background: linear-gradient(90deg, #1E90FF, #DA70D6);
      color: white;
      border: none;
      padding: 12px 25px;
      margin-top: 20px;
      cursor: pointer;
      border-radius: 8px;
      font-size: 16px;
      transition: background 0.3s;
    }
    button:hover {
      background: linear-gradient(90deg, #DA70D6, #1E90FF);
    }
    #resultado {
      margin-top: 20px;
      font-weight: bold;
      font-size: 18px;
      color: #DA70D6;
    }

    /* Footer */
    footer {
      text-align: center;
      padding: 20px;
      background-color: #1E90FF;
      color: white;
    }

  </style>
</head>
<body>

<header>
  <h1>Prevenir es cuidar</h1>
  <nav>
    <a href="#informacion">Información</a>
    <a href="#encuesta">Encuesta</a>
    <a href="#contacto">Contacto</a>
  </nav>
</header>

<section id="informacion">
  <h2>¿Qué son las ITS?</h2>
  <p class="card">Las Infecciones de Transmisión Sexual (ITS) son enfermedades que se transmiten principalmente a través del contacto sexual sin protección. Pueden afectar la salud física y emocional si no se tratan a tiempo.</p>
  
  <h3>Tipos más comunes:</h3>
  <ul class="card">
    <li>Clamidia</li>
    <li>Gonorrea</li>
    <li>VIH/SIDA</li>
    <li>Herpes genital</li>
    <li>Virus del papiloma humano (VPH)</li>
  </ul>

  <h3>Síntomas frecuentes:</h3>
  <ul class="card">
    <li>Secreciones anormales</li>
    <li>Dolor al orinar</li>
    <li>Llagas o verrugas</li>
    <li>Fiebre o malestar general</li>
  </ul>

  <h3>Prevención:</h3>
  <ul class="card">
    <li>Uso de preservativos</li>
    <li>Evitar compartir objetos personales íntimos</li>
    <li>Chequeos médicos regulares</li>
    <li>Educación sexual responsable</li>
  </ul>
</section>

<section id="encuesta">
  <h2>Mini Encuesta</h2>
  <form id="formEncuesta">
    <label>¿Has notado cambios recientes en tu cuerpo?</label>
    <input type="radio" name="q1" value="1"> Sí
    <input type="radio" name="q1" value="0"> No

    <label>¿Tienes secreciones, dolor al orinar o llagas?</label>
    <input type="radio" name="q2" value="1"> Sí
    <input type="radio" name="q2" value="0"> No

    <label>¿Has tenido relaciones sexuales sin protección recientemente?</label>
    <input type="radio" name="q3" value="1"> Sí
    <input type="radio" name="q3" value="0"> No

    <label>¿Sientes dolor, fiebre o malestar general?</label>
    <input type="radio" name="q4" value="1"> Sí
    <input type="radio" name="q4" value="0"> No

    <button type="button" onclick="evaluarEncuesta()">Ver Resultado</button>
    <div id="resultado"></div>
  </form>
</section>

<section id="contacto">
  <h2>Contacto y asistencia</h2>
  <p class="card">Si tus síntomas indican que podrías necesitar asistencia médica, acude a un centro de salud cercano:</p>
  <ul class="card">
    <li>Cruz Roja Paraguaya – Filial Itapúa</li>
    <li>Hospital Regional de Encarnación</li>
    <li>Clínicas privadas con atención en salud sexual</li>
  </ul>
  <p class="card">Recuerda: la prevención y el diagnóstico temprano son clave para tu bienestar.</p>
</section>

<footer>
  &copy; 2025 Prevenir es cuidar. Todos los derechos reservados.
</footer>

<script>
  function evaluarEncuesta() {
    const respuestas = [
      parseInt(document.querySelector('input[name="q1"]:checked')?.value || 0),
      parseInt(document.querySelector('input[name="q2"]:checked')?.value || 0),
      parseInt(document.querySelector('input[name="q3"]:checked')?.value || 0),
      parseInt(document.querySelector('input[name="q4"]:checked')?.value || 0),
    ];
    const total = respuestas.reduce((a,b) => a+b, 0);
    const resultadoDiv = document.getElementById("resultado");

    if(total >= 2){
      resultadoDiv.textContent = "Es recomendable acudir a un profesional de salud para revisión médica.";
    } else {
      resultadoDiv.textContent = "Probablemente sean cambios hormonales normales, pero observa cualquier síntoma que empeore.";
    }
  }
</script>

</body>
</html>
