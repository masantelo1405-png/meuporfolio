[index.html](https://github.com/user-attachments/files/23893631/index.html)
<!DOCTYPE html>
<html lang="pt-br">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>Maria Isabel Santelo - Portfólio</title>
<style>
/* ----- RESET ----- */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

/* ----- ESTILO GERAL ----- */
html, body {
    height: 100%;
    font-family: Arial, sans-serif;
    color: #333;
    scroll-behavior: smooth;

    /* Fundo lilás pastel + textura */
    background-color: #f3e8ff;
    background-image: url('projetos/textura.png'); /* substitua pela sua textura */
    background-repeat: repeat;
    background-size: contain;
    background-position: top left;
}

/* ----- HEADER ----- */
header {
    text-align: center;
    background: rgba(255,255,255,0.85); /* semi-transparente */
    border-bottom: 3px solid #8a2be2;
    padding: 20px 0;
}

header img {
    width: 70%;       /* logo proporcional */
    max-width: 500px; /* limite máximo */
    height: auto;
    display: block;
    margin: 0 auto 15px auto;
    border-radius: 20px;
}

header h1 {
    margin: 10px 0 5px 0;
    color: #8a2be2;
    font-size: 2.5em;
}

header p {
    font-size: 1.2em;
    margin: 0 0 15px 0;
}

/* ----- NAV ----- */
nav {
    display: flex;
    justify-content: center;
    gap: 20px;
    background: rgba(255,255,255,0.85);
    padding: 10px 0;
    position: sticky;
    top: 0;
    z-index: 100;
}

nav a {
    text-decoration: none;
    color: #333;
    font-weight: bold;
    transition: color 0.3s;
}

nav a:hover {
    color: #8a2be2;
}

/* ----- SEÇÕES ----- */
section {
    padding: 50px 20px; /* menos espaço vertical */
    max-width: 1000px;
    margin: auto;
    background: rgba(255,255,255,0.85); /* semi-transparente */
}

/* ----- TÍTULOS ----- */
h2 {
    color: #8a2be2;
    text-align: center;
    margin-bottom: 30px;
}

/* ----- SOBRE ----- */
#sobre p {
    text-align: center;
    font-size: 1.1em;
    line-height: 1.6em;
}

/* ----- HABILIDADES ----- */
.habilidades {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 20px;
}

.habilidade {
    background: #fff;
    border: 2px solid #8a2be2;
    padding: 20px;
    border-radius: 10px;
    width: 200px;
    text-align: center;
    font-weight: bold;
    transition: transform 0.3s;
}

.habilidade:hover {
    transform: translateY(-5px);
}

/* ----- SERVIÇOS ----- */
.servicos {
    display: flex;
    flex-direction: column;
    gap: 20px;
}

.servico {
    background: #fff;
    border-left: 5px solid #8a2be2;
    padding: 15px;
    border-radius: 5px;
}

/* ----- PROJETOS ----- */
#projetos-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 20px;
}

.projeto-link {
    text-decoration: none;
}

.projeto-img {
    width: 250px;
    height: 150px;
    object-fit: cover;
    border-radius: 10px;
    box-shadow: 0 2px 5px rgba(0,0,0,0.2);
    transition: transform 0.3s;
}

.projeto-img:hover {
    transform: scale(1.05);
}

/* ----- FOOTER ----- */
footer {
    text-align: center;
    padding: 20px;
    background: rgba(255,255,255,0.85);
    color: #6a0dad;
}
</style>
</head>
<body>

<header>
    <img src="projetos/logo.png" alt="Logo Maria Isabel">
    <h1>Maria Isabel Santelo</h1>
    <p>Desenvolvedora e Designer | Programação | Informática</p>
</header>

<nav>
    <a href="#sobre">Sobre</a>
    <a href="#habilidades">Habilidades</a>
    <a href="#servicos">Serviços</a>
    <a href="#projetos">Projetos</a>
</nav>

<section id="sobre">
    <h2>Sobre Mim</h2>
    <p>
        Olá! Meu nome é Maria Isabel Santelo. Tenho experiência em design, desenvolvimento web, programação e informática. 
        Sou apaixonada por criar projetos criativos e funcionais, sempre buscando entregar soluções de qualidade.
    </p>
</section>

<section id="habilidades">
    <h2>Habilidades</h2>
    <div class="habilidades">
        <div class="habilidade">Design</div>
        <div class="habilidade">Desenvolvimento Web</div>
        <div class="habilidade">Programação (HTML, Python, PHP, Lua)</div>
        <div class="habilidade">Informática</div>
    </div>
</section>

<section id="servicos">
    <h2>Serviços</h2>
    <div class="servicos">
        <div class="servico">Criação de sites e landing pages</div>
        <div class="servico">Design gráfico e identidade visual</div>
        <div class="servico">Programação de scripts</div>
        <div class="servico">Suporte e consultoria em informática</div>
    </div>
</section>

<section id="projetos">
    <h2>Projetos</h2>
    <div id="projetos-container"></div>
</section>

<footer>
    <p>Entre em contato: santelo.devdesing@gmail.com</p>
    <p>© 2025 Maria Isabel Santelo</p>
</footer>

<script>
document.addEventListener("DOMContentLoaded", function() {
    const pasta = "projetos/";
    const imagens = [
        "projeto1.jpg",
        "projeto2.jpg",
        "projeto3.png",
        "projeto4.png",
        "projeto5.png",
        "projeto6.jpg",
        "projeto7.jpg",
        "projeto8.jpg",
        "projeto9.jpg",
        "projeto10.png",
        "projeto11.png",
        "projeto12.png"
    ];

    const container = document.getElementById("projetos-container");

    imagens.forEach(nome => {
        const link = document.createElement("a");
        link.href = pasta + nome;
        link.target = "_blank";
        link.className = "projeto-link";

        const img = document.createElement("img");
        img.src = pasta + nome;
        img.className = "projeto-img";

        link.appendChild(img);
        container.appendChild(link);
    });
});
</script>

</body>
</html>
[script.js](https://github.com/user-attachments/files/23893633/script.js)
// Caminho da pasta onde estão os projetos
const pasta = "projetos/";

// Lista dos seus 12 projetos (você preenche com os nomes)
const imagens = [
  "projeto1.jpg",
  "projeto2.jpg",
  "projeto3.jpg",
  "projeto4.jpg",
  "projeto5.jpg",
  "projeto6.jpg",
  "projeto7.jpg",
  "projeto8.jpg",
  "projeto9.jpg",
  "projeto10.jpg",
  "projeto11.jpg",
  "projeto12.jpg",
];

// Onde as imagens vão aparecer
const container = document.querySelector("#projetos-container");

// Criar cada imagem automaticamente
imagens.forEach(nome => {
  let img = document.createElement("img");
  img.src = pasta + nome;
  img.className = "projeto-img";
  container.appendChild(img);
});

[style.css](https://github.com/user-attachments/files/23893634/style.css)
/* ----- RESET ----- */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

/* ----- ESTILO GERAL ----- */
html, body {
    height: 100%;
    font-family: Arial, sans-serif;
    color: #333;
    scroll-behavior: smooth;

    /* Fundo lilás pastel + textura leve */
    background-color: #f3e8ff;
    background-image: url('projetos/textura.png'); /* coloque sua textura aqui */
    background-repeat: repeat;
    background-size: contain;
    background-position: top left;
}

/* ----- HEADER ----- */
header {
    text-align: center;
    border-bottom: 3px solid #8a2be2;
    padding: 20px 0;
    background: rgba(255,255,255,0.85); /* semi-transparente para ver a textura */
}

header img {
    width: 90%;        /* logo gigante */
    max-width: 800px;
    height: auto;
    display: block;
    margin: 0 auto 10px auto;
    border-radius: 20px;
}

header h1 {
    margin: 10px 0 5px 0;
    color: #8a2be2;
    font-size: 3em;
}

header p {
    font-size: 1.4em;
    margin: 0 0 20px 0;
}

/* ----- NAV ----- */
nav {
    display: flex;
    justify-content: center;
    gap: 20px;
    background: rgba(255,255,255,0.85);
    padding: 10px 0;
    position: sticky;
    top: 0;
    z-index: 100;
}

nav a {
    text-decoration: none;
    color: #333;
    font-weight: bold;
    transition: color 0.3s;
}

nav a:hover {
    color: #8a2be2;
}

/* ----- SEÇÕES ----- */
section {
    padding: 80px 20px;
    min-height: 100vh;
    background: rgba(255,255,255,0.85); /* semi-transparente para ver textura */
}

/* ----- TÍTULOS ----- */
h2 {
    color: #8a2be2;
    text-align: center;
    margin-bottom: 40px;
}

/* ----- HABILIDADES ----- */
.habilidades {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 20px;
}

.habilidade {
    background: #fff;
    border: 2px solid #8a2be2;
    padding: 20px;
    border-radius: 10px;
    width: 200px;
    text-align: center;
    font-weight: bold;
    transition: transform 0.3s;
}

.habilidade:hover {
    transform: translateY(-5px);
}

/* ----- SERVIÇOS ----- */
.servicos {
    display: flex;
    flex-direction: column;
    gap: 20px;
}

.servico {
    background: #fff;
    border-left: 5px solid #8a2be2;
    padding: 15px;
    border-radius: 5px;
}

/* ----- PROJETOS ----- */
#projetos-container {
    display: flex;
    flex-wrap: wrap;
    justify-content: center;
    gap: 20px;
}

.projeto-link {
    text-decoration: none;
}

.projeto-img {
    width: 250px;
    height: 150px;
    object-fit: cover;
    border-radius: 10px;
    box-shadow: 0 2px 5px rgba(0,0,0,0.2);
    transition: transform 0.3s;
}

.projeto-img:hover {
    transform: scale(1.05);
}

/* ----- FOOTER ----- */
footer {
    text-align: center;
    padding: 20px;
    background: rgba(255,255,255,0.85);
    color: #6a0dad;
}
