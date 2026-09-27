# RobôVerde - Android Site

Site informativo sobre a história e evolução do Android, com sistema de busca em JSON e navegação por parágrafos.

[![Acessar site](https://img.shields.io/badge/acessar-site-3b82f6?style=flat-square)](https://kleinmoretty-coder.github.io/android-site-2.0/)
[![License](https://img.shields.io/badge/license-MIT-green?style=flat-square)](LICENSE)

---

## Sobre o projeto

Projeto desenvolvido durante o Módulo 4 do Curso em Vídeo, refeito posteriormente com foco em organização de código e funcionalidades client-side.

O conteúdo é estruturado em JSON, o que permite um sistema de busca funcional: o usuário pesquisa um termo, o sistema identifica os parágrafos onde ele aparece e libera navegação de "Próximo" e "Anterior", destacando o parágrafo correspondente e fazendo scroll automático até a posição exata.

## Funcionalidades

- Busca em JSON com identificação de termos no conteúdo
- Navegação entre resultados com botões "Próximo" e "Anterior"
- Destaque visual e smooth scroll até o parágrafo encontrado
- Modo escuro com persistência visual
- Menu lateral com lista de tópicos
- Layout responsivo (mobile e desktop)

## Tecnologias

- HTML5
- CSS3 (Grid, Flexbox, variáveis)
- JavaScript (ES Modules, sem framework)
- ESLint + Prettier para padronização

## Estrutura

```
.
├── index.html
├── assets/
│   ├── css/
│   ├── img/
│   └── js/
│       ├── main.js
│       └── modules/
│           ├── pesquisa.js
│           ├── pesquisadados.js
│           ├── botoesPesquisa.js
│           ├── menuFixed.js
│           ├── botaoDark.js
│           ├── titoloMover.js
│           ├── formatarinput.js
│           └── utils.js
├── eslint.config.mjs
└── package.json
```

## Como rodar

A forma mais rápida é usar a versão hospedada:

**[kleinmoretty-coder.github.io/android-site-2.0](https://kleinmoretty-coder.github.io/android-site-2.0/)**

Para rodar localmente, é necessário um servidor HTTP (o projeto usa ES Modules, que não funcionam via `file://`):

```bash
git clone https://github.com/kleinmoretty-coder/android-site-2.0.git
cd android-site-2.0
npx serve .
# ou use a extensão Live Server do VS Code
```

### Lint

```bash
npm install
npm run eslint
```

## Observação

A navegação de busca ainda é **desktop-only**. Essa parte não foi adaptada para mobile na versão atual do projeto.
