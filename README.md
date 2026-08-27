# 🌌 COSMOS — Sistema Solar

## 👨‍💻 Autor

**Gabriel Mendes**
**Turma: 1DES**

---

## 📖 Sobre o projeto

Este projeto é um site interativo sobre o **Sistema Solar**, desenvolvido utilizando apenas tecnologias básicas da Web:

* HTML5
* CSS3
* JavaScript

O objetivo é apresentar informações sobre o Sol e os oito planetas de uma maneira visual, moderna e interativa.

Todo o projeto está concentrado em um único arquivo:

```text
index.html
```

Dentro desse arquivo estão o HTML, o CSS e o JavaScript.

---

# 📁 Estrutura do projeto

```text
sistema-solar/
│
├── index.html
│
└── README.md
```

O arquivo `index.html` contém absolutamente tudo que o site precisa para funcionar.

---

# 🧱 1. HTML

O HTML é responsável pela **estrutura do site**.

No começo do arquivo temos:

```html
<!DOCTYPE html>
<html lang="pt-BR">
```

`<!DOCTYPE html>` informa ao navegador que estamos utilizando HTML5.

Já:

```html
<html lang="pt-BR">
```

indica que o conteúdo está em português do Brasil.

---

## 🔝 Cabeçalho

O site possui um `<header>`:

```html
<header>
    <div class="logo">COS<span>MOS</span></div>

    <nav>
        <a href="#inicio">Início</a>
        <a href="#sistema">Sistema Solar</a>
        <a href="#planetas">Planetas</a>
        <a href="#curiosidades">Curiosidades</a>
    </nav>
</header>
```

O `header` representa o cabeçalho.

Dentro dele existe:

* o nome do site;
* o menu de navegação;
* links para diferentes partes da página.

Os links utilizam `href="#..."` para levar o usuário até uma seção específica.

Por exemplo:

```html
<a href="#planetas">Planetas</a>
```

leva até:

```html
<section id="planetas">
```

---

# 🚀 2. Seção inicial

A primeira parte importante é o `hero`.

```html
<section class="hero" id="inicio">
```

Essa seção funciona como a apresentação principal do site.

Ela contém:

* título;
* descrição;
* botão para explorar;
* botão para conhecer os planetas.

O título principal é:

```html
<h1>
    SISTEMA<br>SOLAR
</h1>
```

O `<br>` quebra a linha entre "SISTEMA" e "SOLAR".

---

# ☀️ 3. Sistema Solar animado

Uma das partes principais do projeto é a representação visual do Sistema Solar.

A estrutura utiliza:

```html
<div class="solar-system">
```

Dentro dela existem as órbitas:

```html
<div class="orbit o1"></div>
<div class="orbit o2"></div>
<div class="orbit o3"></div>
...
<div class="orbit o8"></div>
```

Cada órbita representa aproximadamente a trajetória de um planeta.

O Sol fica no centro:

```html
<div class="sun"></div>
```

---

# 🪐 4. Os planetas

Cada planeta possui um elemento HTML próprio.

Exemplo:

```html
<div class="planet-wrapper speed3">
    <div
        class="planet earth"
        onclick="openPlanet('Terra')">
    </div>
</div>
```

A classe:

```text
planet
```

define características gerais do planeta.

A classe:

```text
earth
```

define a aparência específica da Terra.

Já:

```html
onclick="openPlanet('Terra')"
```

faz o JavaScript executar a função `openPlanet()` quando o usuário clicar na Terra.

O mesmo sistema é utilizado para os outros planetas.

---

# 🎨 5. CSS

O CSS está dentro da própria página, entre:

```html
<style>
```

e:

```html
</style>
```

Ele é responsável por toda a aparência do projeto.

Por exemplo:

```css
body {
    background: #03040b;
    color: #fff;
    font-family: Arial, Helvetica, sans-serif;
}
```

Esse código define:

* cor do fundo;
* cor padrão dos textos;
* fonte utilizada.

---

# 🌌 6. Fundo espacial

O fundo possui gradientes e estrelas criadas com CSS.

```css
.space {
    position: fixed;
    inset: 0;
    background:
        radial-gradient(
            circle at 50% 30%,
            #111936 0%,
            #050817 35%,
            #03040b 75%
        );
}
```

O `radial-gradient()` cria uma transição circular de cores.

As estrelas são criadas utilizando:

```css
radial-gradient(circle, ...)
```

Isso permite criar pequenos pontos que simulam estrelas sem precisar baixar imagens.

---

# ✨ 7. Animação das estrelas

As estrelas possuem uma animação:

```css
animation: starsMove 100s linear infinite;
```

Essa animação chama:

```css
@keyframes starsMove
```

O `@keyframes` determina como um elemento deve mudar ao longo do tempo.

Assim, o fundo parece estar se movimentando.

---

# ☀️ 8. Animação do Sol

O Sol também possui uma animação:

```css
animation: sunPulse 3s ease-in-out infinite;
```

Ela altera o brilho do Sol continuamente.

O resultado é um efeito de pulsação que faz o Sol parecer mais vivo.

---

# 🔄 9. Animação das órbitas

Os planetas utilizam:

```css
@keyframes orbit {
    from {
        transform:
            translate(-50%, -50%)
            rotate(0deg);
    }

    to {
        transform:
            translate(-50%, -50%)
            rotate(360deg);
    }
}
```

Isso faz cada planeta completar uma rotação de 360 graus.

As velocidades são diferentes.

Por exemplo:

```css
.speed1 {
    animation-duration: 5s;
}

.speed8 {
    animation-duration: 45s;
}
```

Assim, cada órbita possui uma velocidade diferente.

---

# 🪐 10. Aparência dos planetas

Os planetas não utilizam imagens externas.

Eles são desenhados usando CSS.

Por exemplo:

```css
.earth {
    width: 23px;
    height: 23px;
    border-radius: 50%;
    background: ...;
}
```

O:

```css
border-radius: 50%;
```

transforma o elemento em um círculo.

Gradientes são usados para criar diferentes cores e detalhes.

---

# 💍 11. Anéis de Saturno

Saturno possui um elemento criado pelo pseudo-elemento:

```css
.saturn::after
```

Ele cria uma segunda forma oval ao redor do planeta.

Isso produz o efeito visual dos anéis.

---

# 🖱️ 12. Efeito ao passar o mouse

Os planetas possuem:

```css
.planet:hover {
    transform:
        translate(-50%, -50%)
        scale(1.4);
}
```

O `:hover` é ativado quando o mouse passa por cima.

O:

```css
scale(1.4)
```

aumenta o planeta.

Também existe:

```css
filter: brightness(1.3);
```

que aumenta o brilho.

---

# 📚 13. Cards dos planetas

Os planetas também são apresentados em cartões.

Exemplo:

```html
<article class="planet-card">
    <div class="planet-preview earth"></div>

    <span class="type">
        Planeta rochoso
    </span>

    <h3>Terra</h3>

    <p>
        Nosso planeta e, até onde sabemos,
        o único mundo com vida.
    </p>
</article>
```

Cada cartão possui:

* representação do planeta;
* tipo do planeta;
* nome;
* descrição.

---

# 🖱️ 14. Interação dos cards

Os cards também podem ser clicados:

```html
onclick="openPlanet('Terra')"
```

Quando o usuário clica, o JavaScript identifica qual planeta foi selecionado.

---

# 🧠 15. JavaScript

O JavaScript fica dentro de:

```html
<script>
```

Ele é responsável pela parte interativa do projeto.

Entre suas funções estão:

* abrir informações dos planetas;
* fechar a janela de informações;
* detectar a tecla ESC;
* detectar cliques;
* criar animações de entrada;
* criar efeito de movimento no fundo.

---

# 🗃️ 16. Banco de informações dos planetas

Os dados são armazenados em um objeto JavaScript:

```javascript
const planets = {
    "Terra": {
        type: "Planeta rochoso",
        description: "...",
        diameter: "12.742 km",
        distance: "149,6 milhões km",
        temperature: "≈ 15 °C",
        moons: "1"
    }
};
```

Isso funciona como uma pequena base de dados.

Cada planeta possui informações próprias.

Por exemplo:

```javascript
diameter: "12.742 km"
```

armazena o diâmetro da Terra.

---

# 🪟 17. Modal dos planetas

Quando o usuário clica em um planeta, uma janela aparece.

Essa janela é chamada de **modal**.

Ela possui:

```html
<div class="modal" id="planetModal">
```

Dentro dela são mostrados:

* nome;
* tipo;
* descrição;
* diâmetro;
* distância do Sol;
* temperatura;
* quantidade de luas.

---

# ⚙️ 18. Função openPlanet()

A função principal é:

```javascript
function openPlanet(name) {
```

Ela recebe o nome do planeta.

Depois:

```javascript
const planet = planets[name];
```

procura os dados daquele planeta dentro do objeto `planets`.

Em seguida, os dados são colocados no HTML.

Exemplo:

```javascript
document.getElementById("modalTitle").textContent =
    name;
```

Isso altera o texto do título da janela.

---

# ❌ 19. Fechar o modal

Para fechar a janela existe:

```javascript
function closePlanet() {
    document
        .getElementById("planetModal")
        .classList.remove("active");
}
```

A classe `active` controla se o modal está visível.

---

# ⌨️ 20. Tecla ESC

O JavaScript também permite fechar a janela pressionando ESC:

```javascript
document.addEventListener("keydown", function(event) {

    if (event.key === "Escape") {
        closePlanet();
    }

});
```

O código verifica qual tecla foi pressionada.

Se for `Escape`, o modal é fechado.

---

# 🖱️ 21. Clicar fora do modal

Também é possível fechar clicando fora da caixa:

```javascript
if (event.target === this) {
    closePlanet();
}
```

Isso melhora a experiência do usuário.

---

# 👀 22. Animação dos elementos

O projeto utiliza `IntersectionObserver`.

Ele permite detectar quando um elemento aparece na tela.

```javascript
const observer = new IntersectionObserver(
    entries => {
        entries.forEach(entry => {
            if (entry.isIntersecting) {
                entry.target.style.opacity = "1";
            }
        });
    }
);
```

Com isso, cards e curiosidades aparecem suavemente conforme o usuário rola a página.

---

# 📱 23. Responsividade

O site também funciona em celulares.

Isso é feito utilizando:

```css
@media(max-width:600px)
```

Dentro desse bloco podemos modificar o layout para telas pequenas.

Por exemplo:

```css
.planets-grid,
.facts {
    grid-template-columns: 1fr;
}
```

No computador os cards aparecem em várias colunas.

No celular eles passam a aparecer um embaixo do outro.

---

# 🧩 24. Por que usar tudo em um HTML?

Neste projeto o HTML, CSS e JavaScript foram colocados juntos para facilitar a entrega e a execução.

Normalmente um projeto profissional seria organizado assim:

```text
index.html
style.css
script.js
```

Mas neste projeto tudo está em:

```text
index.html
```

Isso significa que basta abrir o arquivo no navegador.

Não é necessário instalar:

* Node.js;
* bibliotecas;
* frameworks;
* banco de dados;
* servidor.

---

# ▶️ 25. Como executar

### Passo 1

Crie uma pasta:

```text
sistema-solar
```

### Passo 2

Dentro dela crie:

```text
index.html
```

### Passo 3

Cole o código do projeto dentro do arquivo.

### Passo 4

Salve o arquivo.

### Passo 5

Abra o `index.html` em qualquer navegador moderno.

O site deverá funcionar imediatamente.

---

# 🛠️ Tecnologias utilizadas

## HTML5

Utilizado para criar a estrutura da página.

## CSS3

Utilizado para:

* cores;
* layouts;
* gradientes;
* animações;
* responsividade;
* efeitos;
* planetas;
* órbitas.

## JavaScript

Utilizado para:

* interatividade;
* modais;
* eventos de clique;
* eventos de teclado;
* animações;
* manipulação do DOM;
* informações dos planetas.

---

# 🎯 Objetivo acadêmico

O projeto foi desenvolvido para demonstrar conhecimentos de desenvolvimento Web, principalmente:

* estrutura HTML;
* estilização com CSS;
* animações;
* responsividade;
* JavaScript;
* funções;
* objetos;
* eventos;
* manipulação do DOM.

---

# 👨‍🚀 Resultado

O resultado é uma página interativa sobre o Sistema Solar contendo:

* 🌌 fundo espacial;
* ⭐ estrelas animadas;
* ☀️ Sol;
* 🪐 oito planetas;
* 🔄 órbitas animadas;
* 📱 design responsivo;
* 🖱️ interação com os planetas;
* 📖 informações detalhadas;
* ✨ animações;
* 💻 HTML, CSS e JavaScript em um único arquivo.

---

## 👨‍💻 Créditos

**Projeto desenvolvido por Gabriel Mendes — 1DES**

© 2026 Gabriel Mendes.
