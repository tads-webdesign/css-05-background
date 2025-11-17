# Tutorial CSS 3: Propriedades de Background

## Sumário
1. [Introdução](#introdução)
2. [background-color](#background-color)
3. [background-image](#background-image)
4. [background-size](#background-size)
5. [background-position](#background-position)
6. [Exemplo Completo](#exemplo-completo)
7. [Recursos Avançados](#recursos-avançados)

---

## Introdução

As propriedades de background em CSS 3 permitem estilizar o fundo dos elementos HTML de diversas formas.
Neste tutorial, vamos aprender sobre as principais propriedades: `background-color`, `background-image`, `background-size` e `background-position`.

Cada seção contém explicações e exemplos práticos para você começar a utilizar essas propriedades em seus projetos.

---

## background-color

A propriedade `background-color` define a cor de fundo de um elemento. Você pode usar nomes de cores, valores hexadecimais, RGB, RGBA, HSL ou HSLA.

**Sintaxe**
```css
background-color: valor;
```

[Exemplos de código](exemplos/background-color.html)

**HTML:**
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <title>Exemplo background-color</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="caixa-azul">Fundo azul</div>
    <div class="caixa-rgb">Fundo RGB</div>
    <div class="caixa-rgba">Fundo RGBA (transparente)</div>
</body>
</html>
```

**CSS:**
```css
.caixa-azul {
    background-color: blue;
    padding: 20px;
    margin: 10px;
    color: white;
}

.caixa-rgb {
    background-color: rgb(255, 100, 50);
    padding: 20px;
    margin: 10px;
    color: white;
}

.caixa-rgba {
    background-color: rgba(0, 150, 0, 0.5);
    padding: 20px;
    margin: 10px;
    color: white;
}
```

**Valores comuns**:
- **Nomes de cores:** `red`, `blue`, `green`, `yellow`, etc.
- **Hexadecimal:** `#FF0000`, `#00FF00`, `#0000FF`
- **RGB:** `rgb(255, 0, 0)`
- **RGBA:** `rgba(255, 0, 0, 0.5)` - o último valor é a opacidade

---

## background-image

A propriedade `background-image` permite adicionar uma ou mais imagens como fundo de um elemento.

**Sintaxe**
```css
background-image: url('caminho/para/imagem.jpg');
```

[Exemplos de código](exemplos/background-image.html)

**HTML:**
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <title>Exemplo background-image</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="caixa-imagem">
        <h2>Texto sobre a imagem</h2>
    </div>
    <div class="gradiente">
        <h2>Gradiente CSS</h2>
    </div>
</body>
</html>
```

**CSS:**
```css
.caixa-imagem {
    background-image: url('imagem.jpg');
    height: 300px;
    padding: 20px;
    color: white;
}

.gradiente {
    background-image: linear-gradient(to right, #ff7e5f, #feb47b);
    height: 200px;
    padding: 20px;
    color: white;
}
```

**Opções**:
- **URL de imagem:** `url('foto.jpg')`
- **Gradiente linear:** `linear-gradient(direção, cor1, cor2)`
- **Gradiente radial:** `radial-gradient(forma, cor1, cor2)`
- **Múltiplas imagens:** `url('img1.jpg'), url('img2.jpg')`

---

## background-size

A propriedade `background-size` controla o tamanho da imagem de fundo.

**Sintaxe**
```css
background-size: largura altura;
```

[Exemplos de código](exemplos/background-size.html)

**HTML:**
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <title>Exemplo background-size</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="caixa-cover">background-size: cover</div>
    <div class="caixa-contain">background-size: contain</div>
    <div class="caixa-pixels">background-size: 200px 100px</div>
</body>
</html>
```

**CSS:**
```css
.caixa-cover {
    background-image: url('paisagem.jpg');
    background-size: cover;
    height: 300px;
    margin: 10px;
    border: 2px solid #333;
}

.caixa-contain {
    background-image: url('paisagem.jpg');
    background-size: contain;
    background-repeat: no-repeat;
    height: 300px;
    margin: 10px;
    border: 2px solid #333;
}

.caixa-pixels {
    background-image: url('icone.png');
    background-size: 200px 100px;
    background-repeat: no-repeat;
    height: 300px;
    margin: 10px;
    border: 2px solid #333;
}
```

### Valores comuns:
- **cover:** A imagem cobre toda a área (pode cortar partes)
- **contain:** A imagem cabe completamente na área (pode sobrar espaço)
- **auto:** Tamanho original da imagem
- **Valores específicos:** `200px 100px` ou `50% 80%`

---

## background-position

A propriedade `background-position` define a posição inicial da imagem de fundo.

### Sintaxe
```css
background-position: posição-x posição-y;
```

### Exemplos de código

**HTML:**
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <title>Exemplo background-position</title>
    <link rel="stylesheet" href="style.css">
</head>
<body>
    <div class="pos-center">center center</div>
    <div class="pos-top-right">top right</div>
    <div class="pos-pixels">50px 100px</div>
</body>
</html>
```

**CSS:**
```css
.pos-center {
    background-image: url('logo.png');
    background-repeat: no-repeat;
    background-position: center center;
    height: 300px;
    margin: 10px;
    border: 2px solid #333;
}

.pos-top-right {
    background-image: url('logo.png');
    background-repeat: no-repeat;
    background-position: top right;
    height: 300px;
    margin: 10px;
    border: 2px solid #333;
}

.pos-pixels {
    background-image: url('logo.png');
    background-repeat: no-repeat;
    background-position: 50px 100px;
    height: 300px;
    margin: 10px;
    border: 2px solid #333;
}
```

### Valores comuns:
- **Palavras-chave:** `left`, `right`, `top`, `bottom`, `center`
- **Percentuais:** `50% 50%` (centro)
- **Pixels:** `20px 40px`
- **Combinações:** `left top`, `center bottom`, `right center`

---

## Exemplo Completo

Agora vamos criar um exemplo completo que utiliza todas as propriedades aprendidas.

[Exemplo completo](index.html)

**HTML (index.html):**
```html
<!DOCTYPE html>
<html lang="pt-BR">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title>Tutorial Completo - Background CSS 3</title>
    <link rel="stylesheet" href="exemplo-completo.css">
</head>
<body>
    <header class="cabecalho">
        <h1>Meu Site Profissional</h1>
        <p>Design moderno com CSS 3</p>
    </header>

    <section class="hero">
        <div class="hero-content">
            <h2>Bem-vindo ao Tutorial de Background</h2>
            <p>Aprenda a criar designs incríveis com CSS 3</p>
            <button class="btn-destaque">Saiba Mais</button>
        </div>
    </section>

    <section class="conteudo">
        <div class="card card-1">
            <h3>Background Color</h3>
            <p>Cores sólidas e gradientes</p>
        </div>
        
        <div class="card card-2">
            <h3>Background Image</h3>
            <p>Imagens e padrões</p>
        </div>
        
        <div class="card card-3">
            <h3>Background Size</h3>
            <p>Controle de dimensões</p>
        </div>
    </section>

    <footer class="rodape">
        <p>&copy; 2024 - Tutorial CSS 3 Background</p>
    </footer>
</body>
</html>
```

**CSS (exemplo-completo.css):**
```css
/* Reset básico */
* {
    margin: 0;
    padding: 0;
    box-sizing: border-box;
}

body {
    font-family: Arial, sans-serif;
    line-height: 1.6;
}

/* Cabeçalho com gradiente */
.cabecalho {
    background-color: #2c3e50;
    background-image: linear-gradient(135deg, #667eea 0%, #764ba2 100%);
    color: white;
    text-align: center;
    padding: 40px 20px;
}

.cabecalho h1 {
    font-size: 2.5em;
    margin-bottom: 10px;
}

/* Seção Hero com imagem de fundo */
.hero {
    background-image: url('https://images.unsplash.com/photo-1557683316-973673baf926?w=1200');
    background-size: cover;
    background-position: center center;
    background-repeat: no-repeat;
    height: 500px;
    display: flex;
    align-items: center;
    justify-content: center;
    position: relative;
}

/* Overlay escuro sobre a imagem */
.hero::before {
    content: '';
    position: absolute;
    top: 0;
    left: 0;
    right: 0;
    bottom: 0;
    background-color: rgba(0, 0, 0, 0.5);
}

.hero-content {
    position: relative;
    z-index: 1;
    text-align: center;
    color: white;
}

.hero-content h2 {
    font-size: 3em;
    margin-bottom: 20px;
}

.hero-content p {
    font-size: 1.3em;
    margin-bottom: 30px;
}

.btn-destaque {
    background-color: #e74c3c;
    background-image: linear-gradient(to right, #e74c3c, #c0392b);
    color: white;
    padding: 15px 40px;
    border: none;
    border-radius: 5px;
    font-size: 1.1em;
    cursor: pointer;
    transition: transform 0.3s;
}

.btn-destaque:hover {
    transform: scale(1.05);
}

/* Seção de conteúdo */
.conteudo {
    display: flex;
    justify-content: space-around;
    flex-wrap: wrap;
    padding: 60px 20px;
    background-color: #f4f4f4;
}

.card {
    width: 300px;
    height: 250px;
    margin: 15px;
    padding: 30px;
    border-radius: 10px;
    color: white;
    display: flex;
    flex-direction: column;
    justify-content: center;
    transition: transform 0.3s;
}

.card:hover {
    transform: translateY(-10px);
}

.card-1 {
    background-color: #3498db;
    background-image: linear-gradient(45deg, #3498db, #2980b9);
}

.card-2 {
    background-color: #2ecc71;
    background-image: 
        linear-gradient(rgba(46, 204, 113, 0.8), rgba(46, 204, 113, 0.8)),
        url('data:image/svg+xml,<svg width="60" height="60" xmlns="http://www.w3.org/2000/svg"><circle cx="30" cy="30" r="20" fill="rgba(255,255,255,0.1)"/></svg>');
    background-size: auto, 60px 60px;
    background-position: center, 0 0;
}

.card-3 {
    background-image: 
        radial-gradient(circle, rgba(155, 89, 182, 0.9), rgba(142, 68, 173, 0.9)),
        url('https://images.unsplash.com/photo-1550745165-9bc0b252726f?w=600');
    background-size: cover;
    background-position: center;
}

.card h3 {
    font-size: 1.8em;
    margin-bottom: 15px;
}

/* Rodapé */
.rodape {
    background-color: #34495e;
    background-image: linear-gradient(to bottom, #2c3e50, #34495e);
    color: white;
    text-align: center;
    padding: 30px;
}

/* Responsividade */
@media (max-width: 768px) {
    .hero-content h2 {
        font-size: 2em;
    }
    
    .conteudo {
        flex-direction: column;
        align-items: center;
    }
}
```

---

## Recursos Avançados

### Documentação Oficial
- [MDN Web Docs - CSS Background](https://developer.mozilla.org/pt-BR/docs/Web/CSS/background)
- [W3Schools - CSS Background](https://www.w3schools.com/css/css_background.asp)

### Propriedades Avançadas para Estudo
- **background-repeat:** Controla a repetição da imagem de fundo
- **background-attachment:** Define se a imagem rola com a página (fixed/scroll)
- **background-origin:** Define a área de posicionamento da imagem
- **background-clip:** Define a área de pintura do fundo
- **background (shorthand):** Permite definir todas as propriedades de uma vez

### Ferramentas Úteis
- [CSS Gradient Generator](https://cssgradient.io/) - Gerador de gradientes CSS
- [Unsplash](https://unsplash.com/) - Banco de imagens gratuitas de alta qualidade
- [Coolors](https://coolors.co/) - Gerador de paletas de cores
- [CSS Pattern Gallery](https://projects.verou.me/css3patterns/) - Padrões CSS prontos

### Tutoriais Complementares
- [CSS Tricks - Background](https://css-tricks.com/almanac/properties/b/background/)
- [Gradientes CSS Avançados](https://www.w3schools.com/css/css3_gradients.asp)
- [Multiple Backgrounds](https://developer.mozilla.org/en-US/docs/Web/CSS/CSS_Backgrounds_and_Borders/Using_multiple_backgrounds)

### Próximos Passos
1. Experimente combinar múltiplas imagens de fundo
2. Aprenda sobre animações com background
3. Estude técnicas de parallax scrolling
4. Explore blend modes com backgrounds
5. Pratique com projetos reais

### Exercícios Práticos
1. Crie um cartão de perfil com gradiente no fundo
2. Desenvolva uma landing page com hero image
3. Construa uma galeria com backgrounds diferentes
4. Faça um menu com efeito hover no background
5. Crie um site completo utilizando todas as propriedades aprendidas

---

**Dica Final:** A prática leva à perfeição! Experimente diferentes combinações de propriedades e veja o que funciona melhor para seu projeto. Não tenha medo de testar e errar.

**Bons estudos! 🚀**
