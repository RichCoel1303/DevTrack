# DevTrack

Aplicação web de organização de estudos e tarefas, desenvolvida com HTML5, CSS3 e JavaScript moderno.

## Funcionalidades
- **Conta:** criar conta (nome, e-mail e senha), entrar com e-mail e senha e sair da conta. Cada conta tem as suas próprias tarefas.
- **Persona:** alterar foto, nome, e-mail e senha, e escolher o fundo do app: claro, escuro ou automático.
- **Detalhes da tarefa:** ao clicar numa tarefa dá para escrever anotações, ajustar o prazo e anexar PDF, Word, Excel, PowerPoint, imagens e qualquer outro arquivo (até 50 MB cada). Imagens, PDF e texto podem ser vistos dentro do app.
- Cadastro de tarefas com categoria, prioridade e prazo.
- Validação de formulário.
- Marcar tarefas como concluídas e excluir tarefas.
- Filtros: todas, pendentes e concluídas.
- Indicadores de progresso atualizados dinamicamente.
- Persistência dos dados com `localStorage`.
- Layout responsivo para celular, tablet e desktop.

## Estrutura
```text
DevTrack/
├── login.html / login.js / login.css
├── cadastro.html / cadastro.js
├── index.html                (painel principal)
├── persona.html / persona.js / persona_style.css
├── css/style.css             (visual do painel)
├── css/theme.css             (temas claro/escuro)
├── css/details.css           (detalhes da tarefa e anexos)
├── js/auth.js                (contas e sessão)
├── js/theme.js               (tema)
├── js/app.js, tasks.js, storage.js
├── js/details.js             (anotações e anexos)
├── js/files.js               (arquivos no IndexedDB)
└── README.md
```

## Como executar
1. Baixe ou clone o repositório.
2. Abra a pasta do projeto.
3. Abra `login.html` (ou `index.html`, que leva ao login) no navegador. Para desenvolvimento, você também pode usar a extensão Live Server do VS Code.

Não é necessário instalar dependências.

## Tecnologias e conceitos demonstrados
- HTML semântico e formulários.
- CSS com Grid, Flexbox e media queries (mobile-first).
- JavaScript com funções, objetos, eventos e manipulação do DOM.
- Validação de entradas e prevenção de injeção de HTML.
- `localStorage` para contas e tarefas; `IndexedDB` para os arquivos anexados.
- Senhas guardadas apenas como hash (PBKDF2 + sal), nunca em texto puro.
