<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Pedir Perdón</title>
<style>
  body {
    font-family: Arial, sans-serif;
    text-align: center;
  }
  .mensaje {
    font-size: 24px;
    margin-top: 20px;
  }
  .perdoname {
    font-size: 36px;
    color: red;
    cursor: pointer;
  }
</style>
</head>
<body>
  <div id="mensaje" class="mensaje">¿Me perdonas Natally ?</div>
  <button id="botonSi" onclick="responder('si')">Sí</button>
  <button id="botonNo" onclick="responder('no')" onmousedown="mostrarMasFrases()">No</button>
  
  <div id="masFrases" style="display: none; margin-top: 20px;">
    <p>Entiendo que te sientas así...</p>
    <p>Me arrepiento de mis acciones...</p>
    <p>Puedo hacer lo necesario para enmendarlo...</p>
  </div>

<script>
  function responder(respuesta) {
    if (respuesta === 'si') {
      document.getElementById('mensaje').textContent = '¡sabia q me hibas a perdonar te amo !';
    } else if (respuesta === 'no') {
      document.getElementById('mensaje').textContent = '¿Me perdonas?';
      document.getElementById('botonNo').style.fontSize = '48px';
      document.getElementById('masFrases').style.display = 'block';
    }
  }

  function mostrarMasFrases() {
    document.getElementById('botonNo').onmouseup = function() {
      document.getElementById('botonNo').style.fontSize = '24px';
      document.getElementById('masFrases').style.display = 'none';
    }
  }
</script>

</body>
</html>
