<!doctype html>
<html lang="pt-br">
  <head>
    <meta charset="UTF-8" />
    <meta name="viewport" content="width=device-width, initial-scale=1.0" />
    <link rel="stylesheet" href="styles.css" />
    <title>Imóvel Guide</title>
  </head>
  <body>
    <!-- Conteúdo principal -->
    <div class="conteudo">
      <button id="verTelefoneBtn">Ver Telefone</button>

      <!-- Elemento para exibir telefone formatado -->
      <div id="telefoneFormatado" class="telefone"></div>
    </div>

    <script src="script.js"></script>
  </body>
</html>
/* Adicione estilos conforme necessário */

/* Estilos do telefone formatado */
.telefone {
  color: orange;
  font-weight: bold;
}
// Função para formatar telefone
function formatarTelefone(numero) {
  return `(${numero.slice(0, 2)}) ${numero.slice(2, 8)}-${numero.slice(8)}`;
}

// Adiciona ouvinte de evento ao botão "ver telefone"
document
  .getElementById("verTelefoneBtn")
  .addEventListener("click", function () {
    // Substitua este número pelo número real
    var numeroTelefone = "99999999999";

    // Formata o número e exibe no elemento
    document.getElementById("telefoneFormatado").innerText =
      formatarTelefone(numeroTelefone);
  });
