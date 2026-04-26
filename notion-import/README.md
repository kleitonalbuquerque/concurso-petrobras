# Importacao no Notion

## Opcao 1: importar Markdown

Use esta opcao para levar o plano completo:

1. No Notion, clique em `Import`.
2. Escolha `Markdown & CSV`.
3. Selecione `plano-estudos-petrobras-analista-sistemas.md`.

## Opcao 2: importar CSV como database

Arquivos disponiveis:

- `cronograma-petrobras.csv`: cria uma base com as 12 semanas.
- `revisoes-petrobras.csv`: cria uma base para controlar R0, R1, R2, R3 e R4.

Depois de importar, ajuste as colunas:

- `Status`: transforme em Select.
- `Inicio` e `Fim`: transforme em Date.
- `Prioridade`: transforme em Select.
- `Questoes` e `Acertos`: transforme em Number.

## Sincronizacao automatica

Para criar ou atualizar databases automaticamente pelo Codex, sera necessario fornecer:

- token de integracao do Notion;
- id do database;
- quais campos voce quer manter.

