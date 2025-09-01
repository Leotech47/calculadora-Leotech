---

# 📱 Calculadora Moderna

Uma calculadora interativa desenvolvida em **HTML, CSS e JavaScript**, com design moderno e suporte a múltiplos temas (Escuro, Claro e Neon).

## 🚀 Tecnologias Utilizadas

* **HTML5** → Estrutura da aplicação e definição dos elementos (botões, display, temas).
* **CSS3** → Estilização avançada com `flexbox`, `grid`, `gradientes`, `backdrop-filter` e responsividade para dispositivos móveis.
* **JavaScript (ES6)** → Implementação da lógica da calculadora, manipulação do DOM, tratamento de erros e suporte ao teclado.

## ⚙️ Lógica de Programação

A lógica foi construída para simular o funcionamento de uma calculadora física:

1. **Gerenciamento de Estados:**

   * `currentInput`: número atual digitado.
   * `previousInput`: número anterior armazenado.
   * `operator`: operação matemática selecionada.
   * `shouldResetDisplay`: controle de atualização do display após operações.

2. **Funções principais:**

   * `inputNumber(num)` → insere números.
   * `inputDecimal()` → insere ponto decimal.
   * `inputOperator(op)` → define operador e guarda número anterior.
   * `calculate()` → executa a operação escolhida, com tratamento para erros como divisão por zero.
   * `clearAll()` e `backspace()` → limpar ou apagar o último dígito.
   * `updateDisplay()` → atualiza os displays principal e secundário.

3. **Tratamento de Erros:**

   * Divisão por zero exibe "Erro" e reseta automaticamente após 2 segundos.
   * Resultados não finitos também são tratados.

4. **Suporte ao Teclado:**

   * Números, operadores, Enter, Backspace e Esc são mapeados para interação direta via teclado.

## 🎨 Detalhes do Design

* **Layout centralizado** com fundo em gradiente animado.
* **Display duplo:**

  * Superior → exibe operação em andamento.
  * Principal → mostra o número atual ou resultado.
* **Botões com efeitos:**

  * `hover` e `active` com animações suaves.
  * Diferenciação visual para operadores, igual e limpar.
* **Temas disponíveis:**

  * 🌙 **Escuro** (default)
  * ☀️ **Claro** (tons suaves e leves)
  * ⚡ **Neon** (efeito futurista com brilhos e bordas luminosas)

## 📖 Como Utilizar

1. Abra o arquivo `calculadora_moderna.html` em qualquer navegador moderno.
2. Escolha um **tema** clicando nos ícones 🌙 ☀️ ⚡.
3. Use os **botões** ou o **teclado** para realizar cálculos.

   * `C` → limpa tudo.
   * `⌫` → apaga o último número.
   * `=` ou **Enter** → executa o cálculo.
4. Resultados são exibidos no display principal, enquanto a operação em andamento aparece no secundário.

---

