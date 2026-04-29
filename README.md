# Leitor Markdown Didático

Um leitor pessoal de Markdown feito em **HTML, CSS e JavaScript puro**, pensado para uso em sala de aula, estudo e preparação de materiais didáticos.

O projeto roda localmente ao abrir o arquivo `index.html` no navegador. Não precisa de servidor, build, Node.js, framework ou instalação de dependências.

## Destaques

- Aplicação 100% em um único arquivo HTML.
- Funciona offline por padrão.
- Editor Markdown com visualização automática.
- Modo aula para exibir apenas o conteúdo renderizado.
- Impressão e salvamento em PDF pelo navegador.
- Importação de arquivos `.md` locais.
- Download do Markdown e do HTML renderizado.
- Tema claro e escuro.
- Salvamento automático no `localStorage`.
- Renderização didática de fórmulas simples de Estatística.
- MathJax online opcional para fórmulas em LaTeX.

## Como Usar

1. Baixe ou clone este repositório.
2. Abra o arquivo `index.html` diretamente no navegador.
3. Cole ou carregue um texto em Markdown.
4. Use a visualização para revisar o conteúdo.
5. Ative o modo aula quando quiser mostrar apenas o material renderizado.
6. Use **Imprimir / Salvar em PDF** para gerar uma versão para distribuição.

## Recursos de Markdown

O leitor inclui um parser simples, suficiente para materiais didáticos:

- Títulos com `#`, `##`, `###` e `####`.
- Negrito, itálico e código inline.
- Blocos de código delimitados por três crases ou três tils.
- Listas ordenadas e não ordenadas.
- Citações.
- Linhas horizontais.
- Links.
- Tabelas Markdown.
- Parágrafos com quebras de linha adequadas.

## Fórmulas

O modo padrão é offline. Fórmulas comuns de Estatística são convertidas para uma forma visual usando Unicode e CSS, sem depender de internet.

Exemplos:

| Entrada | Resultado offline |
|---|---|
| `\frac{A}{K}` | `A / K` |
| `\sum f_i = n` | `Σ fᵢ = n` |
| `x_{\max} - x_{\min}` | `xₘáx − xₘín` |
| `650 \leq x < 730` | `650 ≤ x < 730` |

Também há uma opção para ativar **MathJax online**. Se a CDN não estiver disponível, o aplicativo volta automaticamente para o modo offline.

## Uso em Sala

O modo aula oculta o editor e a barra de ferramentas, deixando apenas o conteúdo renderizado em uma tela limpa. Para sair, use o botão flutuante ou a tecla `Esc`.

Para gerar PDF, use o botão **Imprimir / Salvar em PDF** e escolha a opção de salvar como PDF no navegador.

## Estrutura do Projeto

```text
.
├── index.html
├── LICENSE
└── README.md
```

## Privacidade e Segurança

O conteúdo digitado fica no próprio navegador. O aplicativo escapa HTML inserido pelo usuário antes da renderização, evitando a execução de scripts colados no Markdown.

O MathJax só é carregado pela internet se a opção online for ativada manualmente.

## Licença

Este projeto está licenciado sob a licença MIT. Consulte o arquivo [LICENSE](LICENSE).
