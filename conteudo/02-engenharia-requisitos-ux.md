# Engenharia de Software, Requisitos e UX

## Engenharia de Software

Engenharia de Software é a aplicação de métodos, processos, ferramentas e práticas para desenvolver, manter e evoluir software com qualidade, previsibilidade e controle.

O objetivo não é apenas "programar". É entregar software útil, sustentável, testável, seguro e alinhado às necessidades do negócio.

## Ciclos de vida de software

### Cascata

Modelo sequencial. As fases ocorrem em ordem: requisitos, análise, projeto, implementação, testes, implantação e manutenção.

Vantagens:

- simples de entender;
- bom para escopo estável;
- facilita documentação formal.

Desvantagens:

- lida mal com mudanças;
- feedback chega tarde;
- risco de descobrir problema apenas no fim.

Ponto de prova: cascata não significa ausência de controle. Significa sequência rígida e pouca adaptação.

### Iterativo

O produto é refinado por ciclos. A cada iteração, a equipe aprende, ajusta e melhora.

Vantagem principal: reduz incerteza por feedback frequente.

### Incremental

O sistema é entregue em partes funcionais. Cada incremento adiciona capacidade.

Diferença:

- iterativo: melhora por repetição;
- incremental: entrega por partes.

Na prática, muitos métodos são iterativos e incrementais ao mesmo tempo.

### Espiral

Modelo orientado a riscos. Cada ciclo envolve planejamento, análise de riscos, engenharia e avaliação.

É comum em projetos grandes, complexos e incertos.

## Metodologias ágeis

Métodos ágeis valorizam entrega frequente, colaboração com o cliente, adaptação a mudanças e software funcionando.

### Scrum

Scrum organiza trabalho em sprints. Elementos principais:

- Product Owner: maximiza valor do produto;
- Scrum Master: facilita o processo;
- Developers: constroem o incremento;
- Product Backlog: lista priorizada;
- Sprint Backlog: trabalho da sprint;
- Incremento: resultado potencialmente entregável;
- Sprint Planning, Daily Scrum, Review e Retrospective.

Ponto de prova: Scrum não é cascata curta. Ele trabalha com inspeção e adaptação.

### Kanban

Kanban foca fluxo contínuo.

Práticas:

- visualizar o fluxo;
- limitar trabalho em progresso;
- gerenciar fluxo;
- explicitar políticas;
- melhorar continuamente.

Diferença importante:

- Scrum usa sprints e papéis definidos;
- Kanban usa fluxo contínuo e limites de WIP.

## ALM

ALM significa Application Lifecycle Management. Abrange todo o ciclo de vida da aplicação:

- planejamento;
- requisitos;
- desenvolvimento;
- versionamento;
- testes;
- entrega;
- operação;
- manutenção.

ALM é mais amplo que controle de versão. Git é uma ferramenta dentro de um ecossistema de ALM.

## BDD e TDD

### TDD

Test-Driven Development:

1. escrever teste que falha;
2. implementar o mínimo para passar;
3. refatorar mantendo os testes verdes.

Benefícios:

- força design testável;
- reduz regressões;
- cria documentação executável.

### BDD

Behavior-Driven Development descreve comportamento esperado em linguagem próxima ao negócio.

Formato comum:

```text
Dado um contexto
Quando uma ação ocorre
Então um resultado deve acontecer
```

Diferença:

- TDD é mais técnico e orientado a testes;
- BDD é mais colaborativo e orientado ao comportamento do sistema.

## CI/CD e DevOps

### Integração contínua

Integração contínua ocorre quando mudanças de código são integradas com frequência e validadas por build e testes automatizados.

Objetivo: descobrir erro cedo.

### Entrega e implantação contínua

Continuous Delivery: o sistema está sempre pronto para ser implantado, mas a implantação pode exigir aprovação manual.

Continuous Deployment: cada mudança aprovada passa automaticamente até produção.

### DevOps

DevOps é uma cultura e conjunto de práticas que aproxima desenvolvimento e operação.

Práticas comuns:

- automação de build e deploy;
- monitoramento;
- infraestrutura como código;
- observabilidade;
- pipelines;
- feedback rápido.

DevOps não é apenas ferramenta. É colaboração, fluxo e responsabilidade compartilhada.

## BPMN

BPMN é uma notação para modelar processos de negócio.

Elementos básicos:

- evento: algo que acontece;
- atividade: trabalho executado;
- gateway: decisão, paralelismo ou junção;
- fluxo de sequência: ordem das atividades;
- pool/lane: participantes ou áreas.

Ponto de prova: gateway exclusivo escolhe um caminho; gateway paralelo permite caminhos simultâneos.

## Requisitos

Requisito é uma condição ou capacidade que o sistema precisa atender.

### Requisitos funcionais

Descrevem o que o sistema faz.

Exemplos:

- cadastrar usuário;
- emitir relatório;
- validar senha;
- calcular imposto.

### Requisitos não funcionais

Descrevem qualidades, restrições ou atributos.

Exemplos:

- desempenho;
- segurança;
- disponibilidade;
- usabilidade;
- manutenibilidade;
- conformidade.

Erro comum: tratar "o sistema deve responder em até 2 segundos" como funcional. Isso é requisito não funcional de desempenho.

## Elicitação e gerenciamento de requisitos

Elicitar requisitos é descobrir necessidades com stakeholders.

Técnicas:

- entrevistas;
- workshops;
- observação;
- questionários;
- análise de documentos;
- prototipação;
- brainstorming.

Gerenciar requisitos envolve:

- priorizar;
- rastrear;
- controlar mudanças;
- validar;
- manter alinhamento com objetivos.

## Histórias de usuário

Formato comum:

```text
Como [persona/papel],
quero [capacidade],
para [benefício].
```

Exemplo:

> Como analista, quero exportar relatórios para CSV para analisar dados em planilha.

Boa história tem valor de negócio e pode ser testada por critérios de aceitação.

## Critérios de aceitação

Critérios de aceitação definem quando a história está pronta.

Exemplo:

- exportar arquivo em formato CSV;
- incluir cabeçalho;
- respeitar filtros aplicados;
- informar erro se não houver dados.

Critério ruim:

> O sistema deve ser bom.

Critério bom:

> A exportação deve concluir em até 5 segundos para até 10 mil linhas.

## Lean UX, MVP e prototipação

Lean UX trabalha com hipóteses, experimentos e aprendizado rápido.

MVP é a versão mínima para testar uma hipótese de valor. Não é produto malfeito; é produto enxuto para aprender.

Prototipação permite validar ideias antes de investir em implementação completa.

Tipos:

- baixa fidelidade: papel, wireframe simples;
- média fidelidade: fluxo navegável;
- alta fidelidade: aparência próxima do produto final.

## Design thinking

Design thinking é abordagem centrada no usuário para resolver problemas.

Etapas comuns:

- empatia;
- definição do problema;
- ideação;
- prototipação;
- teste.

Ponto de prova: design thinking não começa pela solução. Começa pela compreensão do problema e do usuário.

## Projeto centrado no usuário

Um projeto centrado no usuário considera necessidades, limitações, contexto e objetivos reais dos usuários.

Práticas:

- pesquisa com usuários;
- personas;
- jornadas;
- testes de usabilidade;
- acessibilidade;
- feedback contínuo.

## Storytelling

Storytelling organiza informações em narrativa para comunicar problema, contexto, impacto e solução.

Em produto, ajuda a alinhar equipe e stakeholders sobre a experiência desejada.

## Questões de treino

1. Qual é a diferença entre ciclo iterativo e incremental?
2. Por que o modelo cascata é arriscado em projetos com requisitos instáveis?
3. Scrum e Kanban são equivalentes?
4. Qual é a diferença entre TDD e BDD?
5. CI/CD é sinônimo de DevOps?
6. Requisito de desempenho é funcional ou não funcional?
7. O que torna uma história de usuário testável?
8. MVP significa produto incompleto e sem qualidade?
9. Design thinking começa pela solução?
10. Em BPMN, para que serve um gateway?

## Gabarito comentado

1. Iterativo refina por ciclos; incremental entrega partes funcionais.
2. Porque mudanças e feedback aparecem tarde.
3. Não. Scrum usa sprints e papéis; Kanban foca fluxo contínuo.
4. TDD orienta implementação por testes; BDD descreve comportamento esperado com linguagem compartilhada.
5. Não. CI/CD é prática técnica; DevOps é cultura e conjunto amplo de práticas.
6. Não funcional.
7. Critérios de aceitação claros e verificáveis.
8. Não. MVP é mínimo para testar hipótese, mantendo qualidade suficiente.
9. Não. Começa por empatia e entendimento do problema.
10. Representar decisão, paralelismo ou junção de fluxos.

