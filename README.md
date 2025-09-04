# 📱 Calculadora LeoTech

Uma calculadora interativa profissional desenvolvida em **HTML5, CSS3 e JavaScript ES6**, com design moderno, lógica robusta e funcionalidades avançadas de monitoramento de usuários.

## 🚀 Tecnologias Utilizadas

* **HTML5** → Estrutura semântica da aplicação com elementos organizados e acessíveis
* **CSS3** → Design responsivo com `flexbox`, `grid`, gradientes dinâmicos e animações suaves
* **JavaScript (ES6)** → Lógica de calculadora baseada em estados, integração com APIs externas e suporte completo ao teclado
* **APIs Externas** → Integração com CountAPI e IPApi para funcionalidades de monitoramento

## ⚙️ Arquitetura e Lógica de Programação

### **Sistema de Estados Avançado**
A calculadora utiliza uma arquitetura baseada em estados que simula o funcionamento de calculadoras profissionais:

```javascript
// Estados principais da aplicação
let currentInput = "0";          // Número atual no display
let operator = null;             // Operador matemático ativo
let previousInput = null;        // Número anterior armazenado
let waitingForOperand = false;   // Controle de entrada de dados
```

### **Funções Principais**

1. **`inputNumber(num)`** → Gerencia entrada de números com validação de estados
2. **`inputOperator(nextOperator)`** → Controla operadores com prevenção de inserção consecutiva
3. **`inputDot()`** → Gerencia pontos decimais com validação inteligente
4. **`calculate(firstOperand, secondOperand, operator)`** → Engine de cálculos com tratamento de erros
5. **`performCalculation()`** → Executa operações com validação completa
6. **`clear()`** e **`backspace()`** → Funções de limpeza e edição

### **Principais Melhorias Implementadas**

* ✅ **Prevenção de operadores consecutivos** - Impossibilita inserções como "5+-×÷"
* ✅ **Validação de pontos decimais** - Impede múltiplos pontos no mesmo número
* ✅ **Cálculos seguros** - Tratamento robusto de divisão por zero
* ✅ **Estados consistentes** - Comportamento previsível em todas as operações
* ✅ **Memória de operações** - Sistema que preserva contexto entre cálculos

## 🎨 Design e Interface

### **Layout Profissional**
* **Header** → Branding da LeoTech com logo e identificação
* **Display** → Área de visualização com overflow horizontal para números grandes
* **Teclado** → Grid 4x4 com botões categorizados por função e cor
* **Footer** → Informações do desenvolvedor e dados de monitoramento

### **Sistema de Cores Inteligente**
```css
.btn-number   { background: #6c2eb9; }  /* Números - Roxo */
.btn-operator { background: orange; }    /* Operadores - Laranja */
.btn-equal    { background: #28a745; }  /* Igual - Verde */
.btn-clear    { background: #e0e0e0; }  /* Limpar - Cinza claro */
```

### **Responsividade Completa**
* **Desktop** → Layout otimizado para telas grandes
* **Mobile** → Adaptação automática com botões redimensionados
* **Tablets** → Interface intermediária balanceada

## 🔧 Funcionalidades Avançadas

### **Monitoramento de Usuários**
* **Contador de Visitantes** → Sistema único por sessão usando CountAPI
* **Geolocalização** → Detecção automática de IP e localização via IPApi
* **Data/Hora em Tempo Real** → Atualização contínua a cada segundo

### **Suporte Completo ao Teclado**
```javascript
// Mapeamento completo de teclas
"0-9"      → Entrada de números
"+ - * /" → Operadores matemáticos
"."        → Ponto decimal
"Enter/="  → Executar cálculo
"Backspace"→ Apagar último caractere
"c/C"      → Limpar calculadora
"Escape"   → Reset completo
```

### **Tratamento Robusto de Erros**
* Divisão por zero retorna 0 (comportamento seguro)
* Validação de números não-finitos
* Prevenção de estados inconsistentes
* Recuperação automática de erros

## 📖 Como Utilizar

### **Operação Básica**
1. **Abra** o arquivo `index.html` em qualquer navegador moderno
2. **Digite** números usando botões ou teclado físico
3. **Selecione** operadores (+, -, ×, ÷) para operações
4. **Pressione** `=` ou `Enter` para obter resultados
5. **Use** `C` para limpar ou `⌫` para editar

### **Funcionalidades Especiais**
* **Cálculos Encadeados** → Execute múltiplas operações em sequência
* **Decimais Inteligentes** → Sistema que previne erros de formatação
* **Navegação por Teclado** → Use completamente via teclado físico
* **Monitoramento** → Acompanhe estatísticas de uso no rodapé

## 🌐 Tecnologias de Deploy

### **APIs Integradas**
* **CountAPI** → `https://api.countapi.xyz/` - Contador de visitantes único
* **IPApi** → `https://ipapi.co/json/` - Geolocalização e informações de IP

### **Otimizações de Performance**
* CSS com animações otimizadas usando `transform`
* JavaScript com event delegation eficiente
* Controle de sessão via `sessionStorage`
* Loading states para APIs externas

## 📊 Estrutura do Projeto

```
calculadora-leotech/
│
├── index.html          # Arquivo principal da aplicação
├── logo.png           # Logo da LeoTech (referência)
└── README.md          # Documentação do projeto
```

## 🔗 Links e Deploy

* **GitHub** → [github.com/leotech47](https://github.com/leotech47)
* **Deploy Vercel** → [calculadora-moderna-leotech.vercel.app](https://calculadora-moderna-leotech.vercel.app/)
* **Domínio Próprio** → [calculadoraleotech.com.br](https://calculadoraleotech.com.br)

## 🚀 Melhorias Futuras

- [ ] Histórico de operações
- [ ] Temas personalizáveis
- [ ] Operações científicas avançadas
- [ ] PWA (Progressive Web App)
- [ ] Testes automatizados

---

## 👨‍💻 Desenvolvedor

**Leonardo Silva** - Análise e Desenvolvimento de Sistemas  
Especialista em desenvolvimento web front-end e lógica de programação

### **Contato**
* GitHub: [@leotech47](https://github.com/leotech47)
* Projeto: LeoTech Projects

---

**© 2025 - LeoTech Projects - Análise e Desenvolvimento de Sistemas**  
*Calculadora profissional com tecnologia de ponta e design moderno*
