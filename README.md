<!DOCTYPE html>
<html lang="pt-BR">
<head>
<meta charset="UTF-8">
<meta name="viewport" content="width=device-width, initial-scale=1.0">
<title>João Victor | Dev</title>

<style>
* {
  margin: 0;
  padding: 0;
  box-sizing: border-box;
}

body {
  font-family: 'Segoe UI', sans-serif;
  background: linear-gradient(135deg, #0f172a, #020617);
  color: white;
}

/* NAV */
nav {
  display: flex;
  justify-content: space-between;
  padding: 20px 60px;
}

nav a {
  color: #cbd5f5;
  margin-left: 20px;
  text-decoration: none;
}

/* HERO */
.hero {
  text-align: center;
  padding: 100px 20px 60px;
  animation: fadeUp 1s ease;
}

.hero h1 {
  font-size: 48px;
}

.hero span {
  background: linear-gradient(45deg, #3b82f6, #22d3ee);
  -webkit-background-clip: text;
  -webkit-text-fill-color: transparent;
}

.hero p {
  margin-top: 10px;
  color: #94a3b8;
}

/* SECTIONS */
section {
  max-width: 1000px;
  margin: auto;
  padding: 60px 20px;
}

/* CARDS */
.card {
  background: rgba(255,255,255,0.05);
  backdrop-filter: blur(10px);
  padding: 20px;
  border-radius: 15px;
  transition: all 0.3s ease;
  opacity: 0;
  transform: translateY(30px);
}

.card.show {
  opacity: 1;
  transform: translateY(0);
}

.card:hover {
  transform: translateY(-5px) scale(1.02);
}

/* SKILLS */
.skills {
  display: flex;
  gap: 20px;
  flex-wrap: wrap;
}

.skill {
  flex: 1;
  min-width: 120px;
  text-align: center;
}

.skill img {
  width: 50px;
}

/* PROJECTS */
.projects {
  display: grid;
  grid-template-columns: repeat(auto-fit, minmax(250px,1fr));
  gap: 20px;
}

/* FOOTER */
footer {
  text-align: center;
  padding: 30px;
  color: #94a3b8;
}

/* ANIMAÇÃO */
@keyframes fadeUp {
  from {
    opacity: 0;
    transform: translateY(40px);
  }
  to {
    opacity: 1;
    transform: translateY(0);
  }
}
</style>
</head>

<body>

<nav>
  <h2>JV</h2>
  <div>
    <a href="#">Sobre</a>
    <a href="#">Projetos</a>
  </div>
</nav>

<div class="hero">
  <h1>Eu crio <span>interfaces modernas</span></h1>
  <p>Desenvolvedor Front-End focado em design e performance</p>
</div>

<section>
  <h2>Sobre</h2>
  <div class="card">
    <p>Estou aprendendo e construindo projetos reais para me tornar um desenvolvedor profissional.</p>
  </div>
</section>

<section>
  <h2>Tecnologias</h2>
  <div class="skills">
    <div class="card skill">
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/html5/html5-original.svg">
      <p>HTML</p>
    </div>
    <div class="card skill">
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/css3/css3-original.svg">
      <p>CSS</p>
    </div>
    <div class="card skill">
      <img src="https://cdn.jsdelivr.net/gh/devicons/devicon/icons/javascript/javascript-original.svg">
      <p>JavaScript</p>
    </div>
  </div>
</section>

<section>
  <h2>Projetos</h2>
  <div class="projects">
    <div class="card">
      <h3>Projeto em desenvolvimento</h3>
      <p>Em breve novos projetos serão adicionados aqui.</p>
    </div>
  </div>
</section>

<footer>
  <p>© João Victor</p>
</footer>

<script>
// animação ao aparecer na tela
const cards = document.querySelectorAll('.card');

window.addEventListener('scroll', () => {
  cards.forEach(card => {
    const top = card.getBoundingClientRect().top;
    if (top < window.innerHeight - 50) {
      card.classList.add('show');
    }
  });
});
</script>

</body>
</html>
