# Caderno Digital Inteligente

Sistema web completo de organização de estudos, construído **apenas** com HTML5, CSS3 e JavaScript puro (Vanilla JS). Todos os dados são armazenados no **LocalStorage** do navegador — não há backend, servidor ou banco de dados externo.

## Como usar

1. Baixe ou extraia a pasta `Projeto`.
2. Abra o arquivo `index.html` diretamente no navegador (duplo clique ou arrastar para a aba do navegador).
3. Crie uma conta na tela de cadastro e faça login.
4. Explore o Dashboard, as páginas de conteúdo (Python, Banco de Dados, Engenharia de Software, Segurança), cadastre Aulas Práticas e veja os Relatórios.

Não é necessário instalar nada, rodar servidor local ou usar terminal — basta abrir o `index.html`.

## Estrutura de pastas

```
Projeto/
├── index.html        Tela inicial (redireciona para login ou dashboard)
├── login.html        Tela de login
├── cadastro.html      Tela de criação de conta
├── dashboard.html     Painel com estatísticas e gráficos
├── python.html        Conteúdo didático de Python
├── banco.html         Conteúdo didático de Banco de Dados
├── engenharia.html     Conteúdo didático de Engenharia de Software
├── seguranca.html      Conteúdo didático de Segurança
├── praticas.html       CRUD de Aulas Práticas
├── relatorios.html     Relatórios, filtros, gráficos e exportação
├── perfil.html         Dados do usuário logado
├── css/
│   ├── style.css       Estilos globais, layout, sidebar, cards
│   ├── login.css       Estilos de login/cadastro
│   └── dashboard.css   Estilos do dashboard, gráficos, perfil
├── js/
│   ├── database.js     Camada de acesso ao LocalStorage (usuários, sessão, atividades)
│   ├── utils.js         Funções utilitárias (toasts, modais, sidebar, validações)
│   ├── login.js          Lógica da tela de login
│   ├── cadastro.js       Lógica da tela de cadastro
│   ├── dashboard.js      Lógica de dashboard, práticas, relatórios e perfil
│   └── graficos.js       Geração dos gráficos com Chart.js
└── img/                 Pasta reservada para imagens/ícones adicionais
```

## Funcionalidades

- **Autenticação local**: cadastro e login com validação, sem usuário duplicado.
- **Dashboard**: cartões de estatísticas, gráficos de barras e doughnut, atividades recentes.
- **Conteúdo didático**: páginas de Python, Banco de Dados, Engenharia de Software e Segurança, cada tópico com explicação, exemplo de código e curiosidade.
- **Aulas Práticas**: cadastro, edição, exclusão, pesquisa, filtro por disciplina e ordenação de atividades.
- **Relatórios**: tabela completa com pesquisa em tempo real, filtros, ordenação, gráficos de linha/pizza e exportação para CSV e PDF (via impressão do navegador).
- **Perfil**: dados do usuário logado, com edição de nome e senha.
- **Tema escuro com glassmorphism**, sidebar retrátil, animações suaves, toasts de sucesso/erro e modais de confirmação antes de exclusões.

## Tecnologias

- HTML5, CSS3, JavaScript (Vanilla JS) — sem frameworks.
- [Chart.js](https://www.chartjs.org/) (via CDN) — única biblioteca externa, usada apenas para os gráficos.
- LocalStorage da API Web do navegador para toda a persistência de dados.

## Observações

Este projeto é educacional. As senhas são armazenadas em texto simples no LocalStorage do próprio navegador do usuário, o que é adequado para fins de estudo, mas **não deve ser usado como prática de segurança em sistemas reais com backend**.
