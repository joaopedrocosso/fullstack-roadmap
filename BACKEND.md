# Roadmap de Desenvolvimento Backend para Fullstack

## Sumário
1. [Fundamentos de Backend](#fundamentos-de-backend)
   - [Servidores e Redes](#servidores-e-redes)
   - [Programação Server-Side](#programação-server-side)
   - [Arquitetura de Software](#arquitetura-de-software)
2. [Bancos de Dados](#bancos-de-dados)
   - [Bancos de Dados Relacionais](#bancos-de-dados-relacionais)
   - [Bancos de Dados NoSQL](#bancos-de-dados-nosql)
3. [Autenticação e Segurança](#autenticação-e-segurança)
   - [Autenticação](#autenticação)
   - [Segurança](#segurança)

## 1. Fundamentos de Backend

### 1.1. Servidores e Redes

#### HTTP/HTTPS
- **Protocolos de Comunicação**
  - HTTP vs HTTPS: Diferenças e funcionamento.
  - Códigos de Status HTTP: 200 (OK), 404 (Not Found), 500 (Internal Server Error).
- **Métodos HTTP**
  - GET, POST, PUT, DELETE, PATCH: Definições e idempotência.
  - Segurança e boas práticas.
- **Cabeçalhos HTTP**
  - Content-Type, Authorization, CORS: Uso e configuração.

#### Servidores Web
- **Apache**
  - Configuração básica e módulos (mod_rewrite, mod_ssl).
  - Gerenciamento de hosts virtuais e configurações avançadas.
- **Nginx**
  - Arquitetura e configuração.
  - Load balancing e proxy reverso.
- **IIS**
  - Configuração no Windows.
  - Sites, aplicações e pools de aplicação.

#### DNS e IP
- **Conceitos de DNS**
  - Resolução de nomes, registros A, CNAME, MX.
- **Endereçamento IP**
  - IPv4 vs IPv6, sub-redes, máscara de sub-rede.
- **NAT e DHCP**
  - Gerenciamento de endereços IP.

### 1.2. Programação Server-Side

#### Node.js
- **Fundamentos**
  - Event loop, módulos (fs, http, path), npm.
- **Servidor HTTP**
  - Criação e manipulação de requests e responses.
- **Express.js**
  - Estrutura de rotas, middlewares, tratamento de erros.

#### Python
- **Flask**
  - Criação de APIs RESTful, roteamento, templates Jinja2.
- **Django**
  - Estrutura MVC, ORM, criação e migração de modelos.
  - Manipulação de arquivos, autenticação e autorização (JWT, OAuth).

#### PHP
- **Fundamentos**
  - Sintaxe básica, variáveis, funções, arrays.
- **Laravel**
  - Estrutura MVC, roteamento, middleware, Eloquent ORM.
- **PHP Puro vs Frameworks**
  - Configuração de ambientes (Apache, XAMPP).

### 1.3. Arquitetura de Software

#### MVC (Model-View-Controller)
- **Conceitos Básicos**
  - Separação de responsabilidades e exemplos práticos.
- **Implementação em Frameworks**
  - Django, Laravel, Ruby on Rails.
- **Comparação com Outros Padrões**
  - MVVM, MVP.

#### RESTful APIs
- **Princípios REST**
  - Statelessness, caching, uniform interface.
- **Design de Endpoints RESTful**
  - Uso de verbos HTTP, URIs, versionamento de API.
- **Documentação de APIs**
  - Swagger/OpenAPI.

#### GraphQL
- **Conceitos**
  - Schema, resolvers, queries, mutations.
- **Comparação com REST**
  - Vantagens e desvantagens.
- **Implementação Básica**
  - Apollo Server e integração com frontends.

#### Microservices
- **Arquitetura de Microsserviços**
  - Princípios e comunicação entre serviços (REST, gRPC, RabbitMQ).
- **Gerenciamento de Estados e Banco de Dados**
  - Ferramentas de orquestração: Kubernetes, Docker Swarm.

## 2. Bancos de Dados

### 2.1. Bancos de Dados Relacionais

#### SQL (Structured Query Language)
- **Fundamentos**
  - SELECT, INSERT, UPDATE, DELETE, filtros (WHERE, ORDER BY, GROUP BY).
- **Joins**
  - Inner join, left join, right join, full join.
- **Subqueries e Transações**
  - Controle de concorrência (ACID).

#### MySQL
- **Instalação e Configuração**
  - Criação de bancos e usuários.
- **Procedimentos Armazenados**
  - Triggers, índices, views.
- **Replicação e Backup**
  - Tunning de performance.

#### PostgreSQL
- **Características e Diferenciais**
  - Suporte a tipos avançados (JSON, arrays), extensões.
- **Configuração Básica**
  - Roles e permissões, schemas.
- **Índices e Particionamento**
  - Replicação e sharding.

#### SQLite
- **Uso em Projetos Leves**
  - Embedded systems, configuração e uso.
- **Operações Básicas**
  - Criação de tabelas, inserção e consulta de dados.
- **Ferramentas de Gerenciamento**
  - SQLite Browser, comandos SQL específicos.

### 2.2. Bancos de Dados NoSQL

#### MongoDB
- **Estrutura de Documentos**
  - BSON, coleções e databases.
- **Operações CRUD**
  - Inserção, leitura, atualização, deleção de documentos.
- **Índices e Agregação**
  - Pipelines de dados.

#### Redis
- **Conceitos de Chave-Valor**
  - Uso como cache.
- **Comandos Básicos**
  - SET, GET, EXPIRE, INCR, DECR.
- **Persistência de Dados**
  - Snapshots (RDB), append-only file (AOF).

#### Cassandra
- **Arquitetura Distribuída**
  - Particionamento, consistência eventual.
- **Modelagem de Dados**
  - Keyspaces, tabelas, tipos de dados.
- **Query Language (CQL)**
  - Criação e manipulação de tabelas, inserção e leitura de dados.

## 3. Autenticação e Segurança

### 3.1. Autenticação

#### Sessões e Cookies
- **Conceitos de Sessão**
  - Armazenamento em cookies.
- **Criação e Gerenciamento**
  - Expiração e renovação de sessões.
- **Cookies Seguros**
  - HttpOnly, Secure, SameSite.

#### JSON Web Tokens (JWT)
- **Conceitos**
  - Header, Payload, Signature.
- **Geração e Verificação**
  - Uso de bibliotecas (jsonwebtoken em Node.js, pyjwt em Python).
- **Fluxo de Autenticação com JWT**
  - Renovação de tokens e segurança.

#### OAuth 2.0
- **Fluxo de Autorização**
  - Client credentials, authorization code, implicit, password.
- **Implementação Básica**
  - Autenticação com Google, Facebook, GitHub.
- **OpenID Connect**
  - Extensão de OAuth 2.0 para autenticação.

### 3.2. Segurança

#### Proteção Contra Ataques
- **CSRF (Cross-Site Request Forgery)**
  - Conceitos, tokens anti-CSRF, SameSite cookies.
- **XSS (Cross-Site Scripting)**
  - Tipos de XSS (Reflected, Stored, DOM-based), proteção via sanitização e escape.
- **SQL Injection**
  - Ataques de injeção, preparação de consultas (prepared statements), ORM e proteção automática.

#### Criptografia
- **Criptografia Simétrica e Assimétrica**
  - AES, RSA, uso de bibliotecas (crypto em Node.js, pycryptodome em Python).
- **Hashing Seguro de Senhas**
  - Bcrypt, Argon2, Scrypt.
- **SSL/TLS**
  - Conceitos de criptografia em trânsito, configuração de certificados, força de cifragem.

#### Segurança em APIs
- **Rate Limiting**
  - Proteção contra abuso, ferramentas (express-rate-limit em Node.js, throttle em Django).
- **Segurança em Headers HTTP**
  - Content-Security-Policy, X-Frame-Options, X-XSS-Protection.
- **Auditoria e Logging**
  - Ferramentas de monitoramento, auditoria de acessos e logs.
