# Rotina no Obsidian

## Como abrir

1. Abra o Obsidian.
2. Clique em `Open folder as vault`.
3. Selecione `/storage/projects/concurso-ti/petrobras`.
4. Abra `00-dashboard-petrobras.md`.

## Estrutura recomendada

- Use `00-dashboard-petrobras.md` como pagina inicial.
- Use `plano-estudos-petrobras-analista-sistemas.md` como edital verticalizado.
- Crie uma nota por topico estudado usando `templates/topico-edital.md`.
- Crie uma nota por sessao de estudo usando `templates/sessao-estudo.md`.
- Mantenha o caderno de erros dentro das notas de topico ou em uma nota propria.

## Revisoes

Ao finalizar um topico, registre:

- R0: mesmo dia.
- R1: 24 horas depois.
- R2: 7 dias depois.
- R3: 30 dias depois.
- R4: depois de simulado.

Sugestao de tags:

- `#petrobras`
- `#revisao/r1`
- `#revisao/r2`
- `#erro`
- `#flashcard`
- `#questoes`

## Flashcards

O arquivo `flashcards-petrobras-base.tsv` esta em formato TSV e pode ser importado no Anki.

Configuracao no Anki:

- Tipo: Basic.
- Separador: tab.
- Campo 1: Frente.
- Campo 2: Verso.
- Campo 3: Tags.
- Baralho sugerido: `Petrobras::Analista Sistemas ES`.

## Notion

O Notion pode importar:

- Markdown: importe `plano-estudos-petrobras-analista-sistemas.md`.
- CSV: importe os arquivos dentro de `notion-import/`.

Para sincronizacao automatica com Notion, seria preciso usar a API do Notion com um token de integracao e um database id.

