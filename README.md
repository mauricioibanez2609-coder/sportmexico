<!DOCTYPE html>
<html lang="es">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Sport México | Consultoría Deportiva</title>

<style>
*{margin:0;padding:0;box-sizing:border-box;}
body{font-family:'Segoe UI',sans-serif;background:#f4f4f4;color:#333;scroll-behavior:smooth;}

/* NAV */
nav{
    background:#0a3d2e;
    color:#fff;
    display:flex;
    justify-content:space-between;
    align-items:center;
    padding:15px 20px;
    position:sticky;
    top:0;
    z-index:1000;
}

.logo{font-weight:bold;font-size:1.3rem;}

.menu{display:flex;gap:20px;}
.menu a{color:white;text-decoration:none;font-weight:bold;}

.hamburguesa{
    display:none;
    font-size:25px;
    cursor:pointer;
}

/* HEADER */
header{
    background:linear-gradient(rgba(0,0,0,0.6),rgba(0,0,0,0.6)),
    url('https://images.unsplash.com/photo-1517649763962-0c623066013b');
    background-size:cover;
    background-position:center;
    color:white;
    text-align:center;
    padding:120px 20px;
}

header h1{font-size:3rem;}
header p{margin:15px 0;}

/* BOTONES */
.btn{
    display:inline-block;
    margin:10px;
    padding:12px 20px;
    background:#00c27a;
    color:white;
    border-radius:5px;
    text-decoration:none;
}

.btn:hover{background:#009e63;}

/* SECCIONES */
section{padding:60px 10%;}
h2{color:#0a3d2e;margin-bottom:20px;}

.grid{
    display:grid;
    grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
    gap:20px;
}

.card{
    background:white;
    padding:25px;
    border-radius:15px;
    box-shadow:0 5px 15px rgba(0,0,0,0.1);
    transition:.3s;
}

.card:hover{transform:translateY(-5px);}

/* FOOTER */
footer{
    background:#0a3d2e;
    color:white;
    text-align:center;
    padding:20px;
}

/* BOTON ARRIBA */
#topBtn{
    position:fixed;
    bottom:20px;
    right:20px;
    background:#0a3d2e;
    color:white;
    border:none;
    padding:12px;
    border-radius:50%;
    display:none;
    cursor:pointer;
}

/* RESPONSIVE */
@media(max-width:768px){

.menu{
    display:none;
    flex-direction:column;
    background:#0a3d2e;
    position:absolute;
    top:60px;
    right:0;
    width:200px;
    padding:10px;
}

.menu.active{display:flex;}

.hamburguesa{display:block;}

header h1{font-size:2rem;}
section{padding:40px 20px;}
}
</style>
</head>

<body>

<!-- NAV -->
<nav>
<div class="logo">Sport México</div>

<div class="hamburguesa" onclick="toggleMenu()">☰</div>

<div class="menu" id="menu">
<a href="#nosotros">Nosotros</a>
<a href="#servicios">Servicios</a>
<a href="#empresa">Empresa</a>
<a href="#contacto">Contacto</a>
</div>
</nav>

<!-- HEADER -->
<header>
<h1>Sport México</h1>
<p>Consultoría deportiva profesional enfocada en alto rendimiento</p>

<a class="btn" href="#servicios">Nuestros servicios</a>
<a class="btn" href="https://wa.me/529932332195" target="_blank">Contáctanos</a>
</header>

<!-- NOSOTROS -->
<section id="nosotros">
<h2>¿Quiénes somos?</h2>
<p>
Sport México es una consultoría especializada en el desarrollo integral de atletas, equipos y organizaciones deportivas. 
Nuestro objetivo es maximizar el rendimiento mediante estrategias innovadoras, análisis de datos, tecnología aplicada y entrenamiento personalizado.
</p>

<p>
Trabajamos con metodologías modernas enfocadas en la preparación física, mental y táctica, garantizando resultados medibles y sostenibles en el tiempo.
</p>
</section>

<!-- SERVICIOS -->
<section id="servicios">
<h2>Servicios</h2>

<div class="grid">
<div class="card"><h3>Entrenamiento personalizado</h3><p>Programas adaptados a cada atleta.</p></div>
<div class="card"><h3>Análisis de rendimiento</h3><p>Evaluación con métricas profesionales.</p></div>
<div class="card"><h3>Consultoría deportiva</h3><p>Asesoría para equipos y entrenadores.</p></div>
<div class="card"><h3>Preparación física y mental</h3><p>Desarrollo integral competitivo.</p></div>
<div class="card"><h3>Planificación estratégica</h3><p>Optimización del rendimiento deportivo.</p></div>
<div class="card"><h3>Seguimiento continuo</h3><p>Monitoreo y mejora constante.</p></div>
</div>

</section>

<!-- EMPRESA -->
<section id="empresa">
<h2>Nuestra Empresa</h2>

<div class="grid">
<div class="card"><h3>Misión</h3><p>Impulsar el rendimiento deportivo con estrategias profesionales.</p></div>
<div class="card"><h3>Visión</h3><p>Ser líderes en consultoría deportiva en México.</p></div>
<div class="card"><h3>Valores</h3><p>Disciplina, compromiso, innovación y excelencia.</p></div>
</div>

</section>

<!-- CONTACTO -->
<section id="contacto">
<h2>Contacto</h2>

<p><strong>Mauricio Ibañez De La Cruz</strong><br>
📞 9932332195<br>
<a href="mailto:elpapusport4@gmail.com">Enviar correo</a></p>

<p><strong>Jesus Antonio Ricoy Cruz</strong><br>
📞 993 195 3062</p>

<p><strong>Kevin Alexander Mejia Acosta</strong><br>
📞 932 170 8286</p>

<br>

<a class="btn" href="tel:9932332195">Llamar ahora</a>
<a class="btn" href="mailto:elpapusport4@gmail.com">Enviar correo</a>
</section>

<footer>
<p>© 2026 Sport México | Consultoría Deportiva Profesional</p>
</footer>

<button id="topBtn" onclick="subir()">↑</button>

<script>
function toggleMenu(){
document.getElementById("menu").classList.toggle("active");
}

const btn=document.getElementById("topBtn");

window.onscroll=()=>{
btn.style.display=window.scrollY>200?"block":"none";
}

function subir(){
window.scrollTo({top:0,behavior:"smooth"});
}
</script>

</body>
</html>
