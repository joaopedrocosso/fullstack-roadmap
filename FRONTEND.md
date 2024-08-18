# Frontend Development Roadmap

## Sumário
1. [Fundamentos de HTML e CSS](#fundamentos-de-html-e-css)
   - [HTML (HyperText Markup Language)](#html-hypertext-markup-language)
   - [CSS (Cascading Style Sheets)](#css-cascading-style-sheets)
2. [JavaScript](#javascript)
   - [Fundamentos de JavaScript](#fundamentos-de-javascript)
   - [Manipulação de DOM](#manipulação-de-dom)
   - [Programação Assíncrona](#programação-assíncrona)
3. [Frameworks e Bibliotecas Frontend](#frameworks-e-bibliotecas-frontend)
   - [React](#react)
   - [Vue.js](#vuejs)
   - [Angular](#angular)
   - [Outras Bibliotecas e Ferramentas](#outras-bibliotecas-e-ferramentas)
4. [Responsividade e Design Mobile-First](#responsividade-e-design-mobile-first)
5. [Performance e Otimização de Frontend](#performance-e-otimização-de-frontend)

## 1. Fundamentos de HTML e CSS

### 1.1. HTML (HyperText Markup Language)
#### Elementos e Tags:
- **Estrutura Básica**: `<!DOCTYPE html>`, `<html>`, `<head>`, `<body>`.
- **Tags de Conteúdo**: 
  - Headings (`<h1>` a `<h6>`)
  - Parágrafos (`<p>`)
  - Listas (`<ul>`, `<ol>`, `<li>`)
- **Elementos de Mídia**: 
  - `<img>`: Atributos (`src`, `alt`)
  - `<audio>`, `<video>`: Atributos (`controls`, `src`)
- **Links e Navegação**:
  - `<a>`: Atributos (`href`), Links internos e externos, âncoras.
- **Formulários**:
  - Elementos (`<input>`, `<select>`, `<textarea>`)
  - Tipos de Inputs (`text`, `password`, `email`, `date`)
  - Validação Básica (`required`, `pattern`)
  - Labels e acessibilidade

#### Semântica e Acessibilidade:
- **Elementos Semânticos**:
  - `<header>`, `<footer>`, `<section>`, `<article>`, `<nav>`
- **Acessibilidade**:
  - Uso correto de `alt` em imagens, labels para inputs
  - ARIA roles (`role`, `aria-label`, `aria-hidden`), Navegação por teclado
- **SEO**:
  - Meta tags (`<meta>`, `<title>`, `<meta charset="UTF-8">`, `<meta name="description">`)
  - Estrutura de heading, URLs amigáveis

### 1.2. CSS (Cascading Style Sheets)
#### Seletores e Herança:
- **Seletores Básicos**:
  - Elemento, classe (`.class`), id (`#id`)
  - Pseudo-classes (`:hover`, `:focus`, `:nth-child`)
- **Herança e Cascata**:
  - Ordem de aplicação de estilos, especificidade, uso de `!important`
- **Agrupamento e Combinadores**:
  - Seletores de descendentes, filhos diretos, irmãos adjacentes
- **Resets e Normalização**:
  - CSS resets (normalize.css, reset.css)

#### Box Model e Layout:
- **Conceito de Box Model**:
  - Margem, borda, padding, conteúdo
- **Manipulação de Box Model**:
  - `box-sizing`, `border-box` vs `content-box`, `display` (block, inline-block, inline)
- **Layouts com Float**:
  - Flutuação de elementos, clear fix
- **Flexbox**:
  - Container flex (`display: flex`), eixo principal e cruzado, propriedades (`justify-content`, `align-items`, `flex-wrap`)
- **Grid Layout**:
  - Definição de linhas e colunas, `grid-template-areas`, `grid-gap`, alinhamento (`justify-items`, `align-content`)

#### Estilização Avançada:
- **Cores e Unidades**:
  - Cores (`rgb()`, `rgba()`, `hsl()`, `hex`), Unidades absolutas (px, cm) vs relativas (%, em, rem, vh, vw)
- **Tipografia**:
  - Fontes seguras para a web, importação de fontes externas (`@font-face`, Google Fonts), medidas relativas (em, rem)
- **Animações e Transições**:
  - `transition`, `transform`, `@keyframes`
- **Responsividade**:
  - Media queries (`@media`), design mobile-first, breakpoints comuns

## 2. JavaScript

### 2.1. Fundamentos de JavaScript
#### Sintaxe Básica:
- **Declaração de Variáveis**:
  - `var`, `let`, `const`, escopo (local, global, block scope)
- **Tipos de Dados**:
  - Primitivos (`string`, `number`, `boolean`, `null`, `undefined`, `symbol`, `bigint`)
  - Tipos Complexos (`object`, `array`, `function`)
- **Operadores**:
  - Aritméticos (`+`, `-`, `*`, `/`, `%`), Comparação (`==`, `===`, `!=`, `!==`, `>`, `<`, `>=`, `<=`), Lógicos (`&&`, `||`, `!`)
- **Controle de Fluxo**:
  - Estruturas condicionais (`if`, `else if`, `else`, `switch`), Loops (`for`, `while`, `do...while`)

#### Funções e Escopo:
- **Declaração de Funções**:
  - `function`, `arrow functions` (`() => {}`)
- **Funções Anônimas e Callbacks**:
  - Escopo léxico, closures
- **Funções de Alta Ordem**:
  - Passagem de funções como argumentos, retorno de funções de outras funções
- **Escopo e `this`**:
  - `var`, `let`, `const`, hoisting, conceitos de `this` em diferentes contextos

### 2.2. Manipulação de DOM
#### Seleção de Elementos:
- **Métodos**:
  - `getElementById`, `getElementsByClassName`, `querySelector`, `querySelectorAll`
- **Navegação pelo DOM**:
  - `parentNode`, `childNodes`, `nextSibling`, `previousSibling`
- **Criação e Inserção de Elementos**:
  - `createElement`, `appendChild`, `insertBefore`
- **Manipulação de Atributos e Classes**:
  - `getAttribute`, `setAttribute`, `classList.add`, `classList.remove`, `classList.toggle`

#### Eventos:
- **Manipulação de Eventos**:
  - `addEventListener`, eventos de mouse (`click`, `mouseover`, `mouseout`, `mousemove`), eventos de teclado (`keydown`, `keyup`, `keypress`)
- **Propagação de Eventos**:
  - Capturing vs bubbling, `event.stopPropagation`, `event.preventDefault`
- **Delegação de Eventos**:
  - Uso de eventos delegados para elementos dinâmicos
- **Eventos Customizados**:
  - Criação e disparo de eventos customizados (`new Event`, `dispatchEvent`)

### 2.3. Programação Assíncrona
#### Callbacks e Promises:
- **Funções Assíncronas e Callbacks**:
  - Callback hell, pirâmide da desgraça
- **Promises**:
  - Conceitos básicos (`new Promise`), `resolve`, `reject`, `then`, `catch`, `finally`
  - Manipulação de múltiplas promises (`Promise.all`, `Promise.race`, `Promise.allSettled`, `Promise.any`)

#### Async/Await:
- **Uso de `async` e `await`**:
  - Simplificação de código assíncrono, tratamento de erros com `try...catch`
- **Estruturas de Repetição Assíncronas**:
  - `for await...of`, paralelismo vs serialização de tarefas assíncronas

## 3. Frameworks e Bibliotecas Frontend

### 3.1. React
#### Fundamentos do React:
- **JSX**:
  - Sintaxe JSX, expressões embutidas
- **Componentes**:
  - Componentes funcionais vs de classe, `props`, estado local (`useState`), ciclo de vida de componentes de classe
- **Props e State**:
  - Passagem de props, levantamento de estado, `useEffect`
- **Eventos em React**:
  - Manipulação de eventos em JSX (`onClick`, `onChange`), bind de funções

#### Hooks e Context API:
- **Hooks Básicos**:
  - `useState`, `useEffect`, `useRef`
- **Hooks Avançados**:
  - `useMemo`, `useCallback`, `useReducer`
- **Context API**:
  - Criação de contextos, `useContext`, Provider e Consumer
- **Gerenciamento de Estado Global**:
  - Context API vs bibliotecas externas (Redux, MobX)

### 3.2. Vue.js
#### Fundamentos do Vue.js:
- **Instância do Vue**:
  - Criação, opções (`data`, `methods`, `computed`, `watch`)
- **Templates e Diretivas**:
  - Sintaxe de template (`v-bind`, `v-model`, `v-for`, `v-if`)
- **Componentes**:
  - Componentes locais e globais, `props`, eventos personalizados, slots

#### Vue Router e Vuex:
- **Vue Router**:
  - Configuração de rotas, roteamento dinâmico, parâmetros de rota
- **Vuex**:
  - Conceitos básicos de store, ações, mutações, getters
- **Módulos Vuex**:
  - Organização do store, uso de módulos

### 3.3. Angular
#### Fundamentos do Angular:
- **Estrutura de Projeto**:
  - Módulos, componentes, serviços, injeção de dependência
- **Templates e Diretivas**:
  - Sintaxe de templates, diretivas estruturais (`*ngIf`, `*ngFor`), diretivas de atributos
- **Data Binding e Formulários**:
  - Data binding (`[(ngModel)]`), validação de formulários, formulários reativos

#### Serviços e Dependency Injection:
- **Serviços e Injeção de Dependência**:
  - Criação de serviços, injeção de dependências, hierarquia de injeção
- **RxJS e Observables**:
  - Uso de Observables, operadores RxJS, manipulação de eventos assíncronos

## 4. Responsividade e Design Mobile-First
### Técnicas de Design Responsivo:
- **Media Queries**:
  - Definição de breakpoints, layout adaptativo
- **Design Mobile-First**:
  - Abordagem mobile-first, escalonamento para dispositivos maiores
- **Frameworks de CSS**:
  - Bootstrap, Foundation, Tailwind CSS

## 5. Performance e Otimização de Frontend
### Melhoria de Performance:
- **Minificação e Bundling**:
  - Uso de ferramentas (Webpack, Parcel), otimização de recursos
- **Carregamento Assíncrono**:
  - Lazy loading, carregamento dinâmico de módulos
- **Otimização de Imagens**:
  - Compressão, formatos modernos (WebP, AVIF), responsive images (`<picture>`, `srcset`)

### Boas Práticas:
- **Práticas de Código Limpo**:
  - Manutenção de código, organização de pastas
- **Testes e Debugging**:
  - Testes unitários e de integração (Jest, Mocha), ferramentas de debugging (Chrome DevTools)
