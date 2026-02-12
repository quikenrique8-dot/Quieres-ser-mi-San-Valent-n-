# Quieres-ser-mi-San-Valent-n-
Carta para Alma Isabella 
Html
Copiar código
<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<title>Para Alma Isabella ❤️</title>

<style>
body{
  margin:0;
  font-family: Arial, sans-serif;
  background:linear-gradient(#ff4d6d,#ff8fab);
  color:white;
  text-align:center;
  overflow:hidden;
}

h1{margin-top:30px;}

.card{
  background:white;
  color:#333;
  width:85%;
  max-width:420px;
  margin:20px auto;
  padding:20px;
  border-radius:20px;
  box-shadow:0 10px 25px rgba(0,0,0,0.3);
}

button{
  border:none;
  padding:12px 20px;
  border-radius:20px;
  font-size:18px;
  cursor:pointer;
  margin:10px;
}

.si{background:#ff4d6d;color:white;}
.no{background:#333;color:white;position:relative;}

#mensaje{display:none;margin-top:15px;font-weight:bold;}

.heart{
  position:fixed;
  top:-10px;
  color:red;
  font-size:20px;
  animation:fall linear infinite;
}

@keyframes fall{
  to{transform:translateY(100vh);}
}
</style>
</head>

<body>

<h1>Alma Isabella ❤️</h1>

<div class="card">
<p>Mi amor por ti lleva desde mucho antes que nos hiciéramos novios, sinceramente no recuerdo bien cuándo fue… pero te amo.</p>
<p><b>Desde el 11 de diciembre de 2025</b></p>
<p id="contador"></p>

<h2>¿Quieres ser mi San Valentín?</h2>

<button class="si" onclick="acepto()">SI ❤️</button>
<button class="no" id="noBtn">NO</button>

<p id="mensaje">Sabía que dirías que sí 💕 Te amo muchísimo.</p>
</div>

<!-- Música (puedes cambiar el link por Brillas en YouTube embed) -->
<iframe width="0" height="0"
src="https://www.youtube.com/embed/8i5JuwN7E0A?autoplay=1&loop=1&playlist=8i5JuwN7E0A"
frameborder="0" allow="autoplay"></iframe>

<script>
const fechaInicio = new Date("December 11, 2025 00:00:00").getTime();

function actualizarContador(){
  const ahora = new Date().getTime();
  const diferencia = ahora - fechaInicio;

  const dias = Math.floor(diferencia/(1000*60*60*24));
  const horas = Math.floor((diferencia/(1000*60*60))%24);
  const minutos = Math.floor((diferencia/(1000*60))%60);
  const segundos = Math.floor((diferencia/1000)%60);

  document.getElementById("contador").innerHTML =
  dias+" días "+horas+" horas "+minutos+" minutos "+segundos+" segundos";
}
setInterval(actualizarContador,1000);

function acepto(){
  document.getElementById("mensaje").style.display="block";
}

const noBtn=document.getElementById("noBtn");
noBtn.addEventListener("mouseover",()=>{
  noBtn.style.position="absolute";
  noBtn.style.left=Math.random()*80+"%";
  noBtn.style.top=Math.random()*80+"%";
});

/* corazones cayendo */
function crearCorazon(){
  const heart=document.createElement("div");
  heart.classList.add("heart");
  heart.innerHTML="❤";
  heart.style.left=Math.random()*100+"vw";
  heart.style.animationDuration=(Math.random()*3+2)+"s";
  document.body.appendChild(heart);

  setTimeout(()=>{heart.remove();},5000);
}
setInterval(crearCorazon,300);
</script>

</body>
</html>
