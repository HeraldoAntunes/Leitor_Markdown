# Handoff do Projeto

## Tema

Leitor Markdown Didático: aplicação local em HTML, CSS e JavaScript puro para editar, visualizar, apresentar, imprimir e exportar materiais Markdown com suporte didático a fórmulas simples.

## Status

Projeto funcional em arquivo único. A documentação de contexto foi reorganizada para separar guia humano, regras permanentes de agentes, memória operacional contínua e documento de passagem.

## Complexidade

Baixa a média. O repositório é pequeno, mas `index.html` concentra UI, estilos, parser Markdown, conversor de fórmulas, persistência local e integrações do navegador.

## Objetivo

Manter um leitor Markdown simples, offline por padrão, adequado para uso em sala de aula e preparação de materiais didáticos, sem exigir instalação, servidor ou ferramenta de build.

## Estado Atual

- `index.html` contém toda a aplicação.
- `README.md` descreve uso, recursos, estrutura e arquitetura de contexto.
- `AGENTS.md` define regras permanentes para agentes de IA.
- `docs/PROJECT_STATE.md` é a memória operacional contínua.
- `docs/HANDOFF.md` é este documento de transferência e não deve substituir o estado operacional.
- Não havia `HANDOFF.md` anterior na raiz nem `docs/HANDOFF.md` antigo para converter.

## Artefatos Principais

- `index.html`: app completo.
- `README.md`: documentação para pessoas.
- `AGENTS.md`: regras estáveis para Codex, OpenCode e outros agentes.
- `docs/PROJECT_STATE.md`: estado operacional vivo.
- `docs/HANDOFF.md`: passagem de contexto.
- `LICENSE`: MIT.

## Decisões Tomadas

- Preservar execução local direta via navegador.
- Manter o projeto sem dependências obrigatórias.
- Usar MathJax somente como opção online manual.
- Preservar fallback offline para fórmulas simples de Estatística.
- Usar `localStorage` para persistir conteúdo e tema no navegador.
- Separar contexto do projeto em quatro papéis:
  - `README.md`: guia humano.
  - `AGENTS.md`: regras permanentes de agentes.
  - `docs/PROJECT_STATE.md`: estado operacional atual.
  - `docs/HANDOFF.md`: transferência para outro chat/agente.

## Questões Abertas

- Não existe suíte automatizada de testes.
- A cobertura do parser Markdown e do conversor offline de fórmulas é deliberadamente limitada.
- Ainda falta validar manualmente a aplicação em navegadores após a reorganização documental.
- Pode ser útil criar checklist de QA ou testes unitários leves para o parser, desde que isso não comprometa a simplicidade do projeto.

## Restrições

- Não incluir credenciais, chaves, tokens, senhas, dados pessoais, documentos de alunos, documentos institucionais sensíveis, logs ou temporários.
- Não introduzir dependências obrigatórias sem necessidade clara.
- Não quebrar o uso offline nem a abertura direta de `index.html`.
- Não usar `docs/HANDOFF.md` como memória operacional principal.
- Não alterar `AGENTS.md` automaticamente no futuro sem pedido explícito do usuário.

## Estilo e Preferências Relevantes

- Documentação em português brasileiro claro.
- Foco em uso didático e prático.
- Preferência por simplicidade operacional: abrir o HTML e usar.
- Nenhuma preferência pessoal sensível do usuário está documentada no projeto.

## Próximo Passo Recomendado

Executar uma validação manual no navegador abrindo `index.html` e testando os fluxos principais: edição, visualização, modo aula, impressão/PDF, importação `.md`, downloads, tema e MathJax opcional.

## Instruções para a Próxima IA

1. Leia `README.md`, `AGENTS.md` e `docs/PROJECT_STATE.md` antes de qualquer alteração não trivial.
2. Leia este `docs/HANDOFF.md` apenas quando houver retomada de contexto, continuidade de sessão ou passagem para outro agente.
3. Consulte `index.html` para confirmar comportamento real antes de documentar ou alterar funcionalidades.
4. Atualize `docs/PROJECT_STATE.md` quando houver mudança relevante de estado, decisão, teste, limitação ou próximo passo.
5. Atualize `docs/HANDOFF.md` quando o usuário pedir handoff ou quando uma tarefa terminar em ponto claro de passagem.
