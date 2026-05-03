# Estado Operacional do Projeto

Última atualização: 2026-05-03.

## Objetivo do Projeto

O projeto é um leitor Markdown didático para uso local em sala de aula, estudo e preparação de materiais. Ele roda ao abrir `index.html` no navegador, sem servidor, build, framework, Node.js ou instalação de dependências.

## Estado Atual

- Aplicação funcional em arquivo único: `index.html`.
- Interface com editor Markdown, visualização renderizada, modo aula, impressão/salvamento em PDF pelo navegador, importação de arquivo `.md`, download do Markdown, download/cópia do HTML renderizado, tema claro/escuro e contador de texto.
- Parser Markdown próprio cobre recursos básicos: títulos, ênfase, código inline, blocos de código, listas, citações, linhas horizontais, links, tabelas e parágrafos.
- Fórmulas simples de Estatística são renderizadas offline por conversão para Unicode/CSS.
- MathJax online pode ser ativado manualmente e usa CDN apenas quando a opção é marcada.
- Conteúdo e tema são salvos no `localStorage`.
- Arquitetura de contexto para agentes foi padronizada com `AGENTS.md`, `docs/PROJECT_STATE.md` e `docs/HANDOFF.md`.
- `CLAUDE.md` foi criado como adaptador curto para Claude Code / Claude Desktop, apontando para `AGENTS.md` como fonte principal de regras compartilhadas.

## Estrutura Real do Repositório

```text
.
├── AGENTS.md
├── CLAUDE.md
├── docs
│   ├── HANDOFF.md
│   └── PROJECT_STATE.md
├── index.html
├── LICENSE
└── README.md
```

Não há `.gitignore` no estado atual do repositório.

## Arquivos Principais

- `index.html`: aplicação completa com HTML, CSS e JavaScript.
- `README.md`: guia humano do projeto, uso, recursos, estrutura e arquitetura de contexto.
- `AGENTS.md`: regras permanentes para agentes de IA.
- `CLAUDE.md`: adaptador para Claude Code / Claude Desktop que referencia `AGENTS.md` sem duplicar suas regras.
- `docs/PROJECT_STATE.md`: memória operacional contínua do projeto.
- `docs/HANDOFF.md`: passagem de contexto para outro chat, agente ou sessão.
- `LICENSE`: licença MIT.

## Decisões em Vigor

- Manter o projeto simples e local-first.
- Preservar a execução direta de `index.html` no navegador.
- Evitar dependências obrigatórias.
- Tratar MathJax como recurso online opcional, com fallback offline.
- Escapar HTML fornecido pelo usuário antes da renderização.
- Adotar arquitetura suficiente: evitar overengineering, camadas e abstrações sem dor concreta ou justificativa explícita.
- Usar `docs/PROJECT_STATE.md` como memória operacional contínua.
- Usar `docs/HANDOFF.md` apenas para transferência de contexto.
- Usar `CLAUDE.md` apenas como adaptador para Claude, mantendo `AGENTS.md` como fonte principal de regras compartilhadas.
- Não alterar `AGENTS.md` no futuro sem pedido explícito do usuário.

## Limitações Conhecidas

- O parser Markdown é próprio e didático; não cobre toda a especificação CommonMark.
- A renderização offline de fórmulas cobre casos simples e recorrentes de Estatística, não LaTeX completo.
- Não há suíte automatizada de testes no repositório.
- Testes funcionais dependem de validação manual em navegador.
- O MathJax online depende de disponibilidade de internet e da CDN configurada.

## Testes Feitos

- Varredura completa dos arquivos versionados e não versionados fora de `.git`.
- Leitura de `README.md`, `LICENSE` e `index.html`.
- Busca por referências a `HANDOFF`, `PROJECT_STATE`, `AGENTS`, memória operacional e contexto.
- Verificação de que não havia `AGENTS.md`, `docs/`, `docs/HANDOFF.md`, `docs/PROJECT_STATE.md`, `.gitignore` ou `HANDOFF.md` na raiz antes desta reorganização documental.
- Verificação de `git status --short` antes das alterações: árvore limpa.
- Revisão documental de `README.md`, `AGENTS.md`, `docs/PROJECT_STATE.md` e `docs/HANDOFF.md` antes de registrar a diretriz permanente contra overengineering.
- Verificação de `git status --short` antes da criação de `CLAUDE.md`: árvore limpa.
- Criação documental de `CLAUDE.md` sem alterar arquivos de código.

## Testes Pendentes

- Abrir `index.html` em navegador e validar fluxo principal: editar Markdown, visualizar, alternar modos, imprimir/salvar PDF, carregar `.md`, baixar Markdown e HTML renderizado.
- Validar tema claro/escuro e persistência via `localStorage`.
- Validar fallback offline de fórmulas e ativação manual do MathJax online.
- Testar exemplos de tabelas, listas, links, blocos de código e fórmulas inline/bloco.

## Próximos Passos

- Considerar uma página simples de testes manuais ou checklist de QA para releases.
- Avaliar se vale criar testes automatizados leves para funções puras do parser Markdown, sem introduzir build obrigatório.
- Revisar acessibilidade da barra de ferramentas em telas pequenas.
- Documentar exemplos adicionais de fórmulas suportadas offline, se o uso em sala exigir.

## Instrução de Retomada Rápida

Para retomar o projeto, leia nesta ordem: `README.md`, `AGENTS.md`, `docs/PROJECT_STATE.md` e, se a tarefa envolver continuidade entre sessões ou outro agente, `docs/HANDOFF.md`. Depois consulte `index.html` para confirmar o comportamento executável antes de alterar qualquer coisa.
