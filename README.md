# Primeiro-site
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Beauty Glow | Maquiagem</title>

    <link rel="stylesheet" href="style.css">
</head>
<body>

<header>
    <h1>Beauty Glow</h1>
    <nav>
        <a href="#inicio">Início</a>
        <a href="#dicas">Dicas</a>
        <a href="#produtos">Produtos</a>
        <a href="#contato">Contato</a>
    </nav>
</header>

<section id="inicio" class="hero">
    <div class="texto">
        <h2>Realce sua beleza ✨</h2>
        <p>
            Descubra dicas, tendências e inspirações para criar maquiagens incríveis para qualquer ocasião.
        </p>

        <a href="#dicas" class="botao">
            Ver Dicas
        </a>
    </div>
</section>

<section id="dicas">

<h2>Dicas de Maquiagem</h2>

<div class="cards">

<div class="card">
<h3>💄 Pele</h3>
<p>Prepare a pele com limpeza, hidratação e primer antes da maquiagem.</p>
</div>

<div class="card">
<h3>👁️ Olhos</h3>
<p>Esfume bem as sombras para um acabamento profissional.</p>
</div>

<div class="card">
<h3>💋 Lábios</h3>
<p>Use lápis labial antes do batom para maior duração.</p>
</div>

</div>

</section>

<section id="produtos">

<h2>Produtos Favoritos</h2>

<div class="cards">

<div class="card">
<h3>Base</h3>
<p>Cobertura leve e acabamento natural.</p>
</div>

<div class="card">
<h3>Máscara de Cílios</h3>
<p>Volume e definição para qualquer look.</p>
</div>

<div class="card">
<h3>Batom Matte</h3>
<p>Longa duração e cores incríveis.</p>
</div>

</div>

</section>

<section id="contato">

<h2>Contato</h2>

<form>

<input type="text" placeholder="Seu nome">

<input type="email" placeholder="Seu e-mail">

<textarea placeholder="Sua mensagem"></textarea>

<button>Enviar</button>

</form>

</section>

<footer>

<p>© 2026 Beauty Glow • Todos os direitos reservados.</p>

</footer>

<script src="script.js"></script>

</body>
</html>

*{
margin:0;
padding:0;
box-sizing:border-box;
font-family:Arial,Helvetica,sans-serif;
}

body{
background:#fff8fb;
color:#333;
}

header{
background:#ffb6c1;
display:flex;
justify-content:space-between;
align-items:center;
padding:20px 10%;
position:sticky;
top:0;
}

header h1{
color:white;
}

nav a{
color:white;
text-decoration:none;
margin-left:20px;
font-weight:bold;
}

.hero{
height:90vh;
display:flex;
justify-content:center;
align-items:center;
text-align:center;
background:linear-gradient(rgba(255,255,255,.5),rgba(255,255,255,.5)),
url("https://images.unsplash.com/photo-1522335789203-aabd1fc54bc9?auto=format&fit=crop&w=1500&q=80");
background-size:cover;
background-position:center;
}

.hero h2{
font-size:55px;
margin-bottom:20px;
}

.hero p{
font-size:20px;
margin-bottom:30px;
}

.botao{
background:#ff4f87;
color:white;
padding:15px 35px;
text-decoration:none;
border-radius:30px;
}

section{
padding:80px 10%;
}

section h2{
text-align:center;
margin-bottom:40px;
font-size:40px;
color:#ff4f87;
}

.cards{
display:grid;
grid-template-columns:repeat(auto-fit,minmax(250px,1fr));
gap:25px;
}

.card{
background:white;
padding:30px;
border-radius:15px;
box-shadow:0 10px 20px rgba(0,0,0,.1);
transition:.3s;
}

.card:hover{
transform:translateY(-10px);
}

form{
max-width:600px;
margin:auto;
display:flex;
flex-direction:column;
gap:20px;
}

input,textarea{
padding:15px;
border-radius:10px;
border:1px solid #ccc;
}

textarea{
height:150px;
resize:none;
}

button{
padding:15px;
background:#ff4f87;
color:white;
border:none;
border-radius:10px;
font-size:18px;
cursor:pointer;
}

button:hover{
background:#ff2c6d;
}

footer{
background:#ffb6c1;
text-align:center;
padding:20px;
color:white;
margin-top:50px;
}
const links = document.querySelectorAll("nav a");

links.forEach(link => {
    link.addEventListener("click", e => {
        e.preventDefault();

        const id = link.getAttribute("href");

        document.querySelector(id).scrollIntoView({
            behavior: "smooth"
        });
    });
});

document.querySelector("form").addEventListener("submit", function(e){
    e.preventDefault();

    alert("Mensagem enviada com sucesso! 💖");

    this.reset();
});