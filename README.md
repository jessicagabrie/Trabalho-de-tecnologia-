# Trabalho-de-tecnologia-
document.addEventListener('DOMContentLoaded', function () {  
    const botaoDeAcessibilidade = document.getElementById('botao-acessibilidade')
    const opcoesDeAcessibilidade = document.getElementById('opcoes-acessibilidade')

    botaoDeAcessibilidade.addEventListener('click', function () {
        botaoDeAcessibilidade.classList.toggle('rotacao-botao');
        opcoesDeAcessibilidade.classList.toggle('apresenta-lista')

    })

    const aumentaFonteBotao = document.getElementById('aumentar-fonte');
    const diminuiFonteBotao = document.getElementById('diminuir-fonte');

    const alternaContraste = document.getElementById('alterna-contraste')

    let tamanhoAtualFonte = 1;

    aumentaFonteBotao.addEventListener('click', function () {
        tamanhoAtualFonte += 0.1;
        document.body.style.fontSize = `${tamanhoAtualFonte}rem`

    })

    diminuiFonteBotao.addEventListener('click', function () {
        tamanhoAtualFonte -= 0.1;
        document.body.style.fontSize = `${tamanhoAtualFonte}rem`

    })

    alternaContraste.addEventListener('click', function () {
        document.body.classList.toggle('alto-contraste')
    })


})
<a href="#conteudo" class="skip-link">Pular para o conteúdo principal</a>

<style>
  .skip-link {
    position: absolute;
    left: -999px;
    top: auto;
    background: #000;
    color: #fff;
    padding: 8px;
  }
  .skip-link:focus {
    left: 10px;
    top: 10px;
  }
</style>

<main id="conteudo">
  <h1>Bem-vindo ao site acessível</h1>
</main>
<nav aria-label="Menu principal">
  <ul>
    <li><a href="#home">Início</a></li>
    <li><a href="#sobre">Sobre</a></li>
    <li><a href="#contato">Contato</a></li>
  </ul>
</nav>

<button aria-label="Abrir menu de navegação">☰</button>
<button onclick="toggleContraste()">Ativar/Desativar Alto Contraste</button>

<script>
  function toggleContraste() {
    document.body.classList.toggle("alto-contraste");
  }
</script>

<style>
  .alto-contraste {
    background-color: black;
    color: yellow;
  }
  .alto-contraste a {
    color: cyan;
  }
</style><button onclick="toggleDaltonismo()">Simular Daltonismo</button>

<script>
  function toggleDaltonismo() {
    document.body.classList.toggle("daltonismo");
  }
</script>

<style>
  .daltonismo {
    filter: grayscale(100%);
  }
</style>
<form>
  <label for="nome">Nome:</label>
  <input type="text" id="nome" aria-required="true">

  <label for="email">E-mail:</label>
  <input type="email" id="email" aria-required="true">

  <button type="submit">Enviar</button>
</form>
