# 📱 Calculadora LeoTech

Uma calculadora interativa desenvolvida em **HTML, CSS e JavaScript**, com design moderno e suporte a múltiplos temas (Escuro e Claro).

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

## 📖 Como Utilizar

1. Abra o arquivo index.html em qualquer navegador moderno.

2. Use os botões ou teclado para inserir números e operações.

3. Clique em `=` ou pressione **Enter** para calcular o resultado.

4. Use **`C`** para limpar o display ou **`⌫`** para apagar o último caractere.

6. Alterne entre modo claro e escuro clicando no ícone no canto superior direito.

   **`C`** → limpa tudo.
   **`⌫`** → apaga o último número.
   **`=`** ou **Enter** → executa o cálculo.
4. Resultados são exibidos no display principal, enquanto a operação em andamento aparece no secundário.

---
## Créditos

Desenvolvido por **Leonardo Silva**

[github.com/leotech47](https://github.com/leotech47)

[Projeto - calculadora Leotech no Vercel](https://calculadora-moderna-leotech.vercel.app/)

[Visite o projeto calculadora Leotech na internet](https://calculadoraleotech.com.br)

**© 2025 Calculadora LeoTech**
