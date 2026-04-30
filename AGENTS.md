# AGENTS.md

Guia permanente para agentes de IA que trabalhem neste repositório.

Este arquivo define regras estáveis de trabalho. Ele não é diário de bordo, memória operacional nem resumo de sessão. Não altere este arquivo automaticamente em tarefas futuras; recomende mudanças quando regras permanentes precisarem evoluir, mas só edite `AGENTS.md` se o usuário pedir explicitamente.

## Hierarquia de Contexto

Ao interpretar o projeto, siga esta ordem de prioridade:

1. Instrução explícita do usuário na conversa atual.
2. `AGENTS.md`.
3. `docs/PROJECT_STATE.md`.
4. `docs/HANDOFF.md`.
5. `README.md`.
6. Código real do projeto como fonte final de comportamento executável.

`docs/HANDOFF.md` não substitui `docs/PROJECT_STATE.md`. O handoff serve para transferência de contexto entre chats, sessões ou agentes. `docs/PROJECT_STATE.md` é a memória operacional contínua do projeto.

Se houver divergência sobre comportamento executável, confirme no código real antes de decidir.

## Rotina de Leitura

Ao iniciar qualquer tarefa não trivial, leia:

1. `README.md`.
2. `AGENTS.md`.
3. `docs/PROJECT_STATE.md`.
4. `docs/HANDOFF.md`, se a tarefa envolver retomada de contexto, passagem para outro chat ou continuidade de sessão.
5. Arquivos diretamente relacionados à tarefa.

Para tarefas simples e localizadas, ainda verifique os arquivos afetados antes de editar.

## Rotina de Encerramento

Ao finalizar uma alteração relevante:

1. Avalie se `docs/PROJECT_STATE.md` precisa ser atualizado.
2. Atualize `docs/PROJECT_STATE.md` quando houver mudança de estado, decisão, comportamento, limitação, teste ou próximo passo.
3. Atualize `docs/HANDOFF.md` quando o usuário pedir handoff ou quando a tarefa gerar um ponto claro de passagem para outro chat ou agente.
4. Recomende atualização de `AGENTS.md` quando regras permanentes tiverem mudado, mas não altere `AGENTS.md` sem pedido explícito.

## Regras do Projeto

- O projeto é um leitor Markdown didático em arquivo único, implementado em `index.html` com HTML, CSS e JavaScript puro.
- Não introduza build, framework, dependência ou servidor sem necessidade clara e sem compatibilidade com a proposta offline do projeto.
- Preserve o funcionamento local ao abrir `index.html` diretamente no navegador.
- Não altere arquivos de código quando a tarefa for exclusivamente documental, salvo ajuste mínimo para corrigir referência quebrada.
- Prefira mudanças pequenas, revisáveis e coerentes com a simplicidade do projeto.
- Mantenha a documentação em português brasileiro claro, salvo pedido diferente do usuário.
- Não coloque `AGENTS.md`, `docs/PROJECT_STATE.md` ou `docs/HANDOFF.md` no `.gitignore`.

## Segurança e Privacidade

- Não incluir chaves de API, tokens, senhas, credenciais, dados pessoais, dados sensíveis, documentos de alunos, documentos institucionais sensíveis, logs ou arquivos temporários na documentação ou no código.
- O aplicativo deve continuar escapando conteúdo inserido pelo usuário antes da renderização HTML.
- Qualquer recurso online deve ser opcional e documentado. Atualmente, MathJax online é opcional.
- Preserve a política de privacidade local: o conteúdo do usuário fica no navegador via `localStorage`.

## Documentação

- `README.md` é o guia para pessoas: visão geral, uso, recursos, estrutura e contexto básico.
- `docs/PROJECT_STATE.md` é o estado operacional vivo: estado atual, decisões, limitações, testes, pendências e próximos passos.
- `docs/HANDOFF.md` é o documento de passagem de contexto para outro chat, agente ou sessão.
- Não use `docs/HANDOFF.md` como memória operacional principal.
- Se encontrar referência antiga tratando `docs/HANDOFF.md` como memória operacional, atualize para `docs/PROJECT_STATE.md`.

## Git e Conduta do Agente

- Antes de editar, verifique o estado do Git e preserve mudanças existentes do usuário.
- Não faça commit, push, reset ou limpeza destrutiva sem pedido explícito.
- Não reverta alterações de terceiros ou do usuário sem autorização.
- Ao final, informe arquivos criados, alterados ou movidos e testes executados.
- Quando não puder executar um teste relevante, registre a limitação com clareza.
