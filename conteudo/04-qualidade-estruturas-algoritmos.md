# Qualidade, Testes, Estruturas de Dados e Algoritmos

## Qualidade de software

Qualidade de software é a capacidade de um produto atender requisitos explícitos e implícitos com confiabilidade, segurança, desempenho, usabilidade e manutenibilidade.

Qualidade não é só ausência de defeitos. Também envolve:

- adequação ao uso;
- facilidade de manutenção;
- segurança;
- desempenho;
- testabilidade;
- conformidade.

## Garantia da qualidade e controle da qualidade

Garantia da qualidade é preventiva. Define processos para evitar defeitos.

Controle da qualidade é avaliativo. Verifica se o produto atende padrões e requisitos.

Exemplo:

- garantia: definir revisão de código obrigatória;
- controle: executar testes e inspeções.

## Controle de versão e Git

Git registra histórico de alterações.

Conceitos:

- commit: registro de mudança;
- branch: linha de desenvolvimento;
- merge: integração de branch;
- rebase: reaplicação de commits;
- tag: marcação de versão;
- remote: repositório remoto.

Boas práticas:

- commits pequenos;
- mensagens claras;
- revisão antes de merge;
- evitar commits de arquivos temporários;
- usar branches para trabalho isolado.

## Tipos de teste

### Teste unitário

Valida uma unidade pequena, como função, método ou classe.

Características:

- rápido;
- isolado;
- automatizável;
- ajuda a refatorar com segurança.

### Teste de integração

Valida interação entre componentes.

Exemplos:

- API com banco de dados;
- serviço com fila;
- módulo de autenticação com cadastro.

### Teste funcional

Verifica funcionalidade do ponto de vista de requisito.

### Teste de aceitação

Confirma se o sistema atende necessidades de negócio e critérios definidos.

### Teste de desempenho

Avalia tempo de resposta, vazão e uso de recursos.

### Teste de carga

Verifica comportamento sob volume esperado ou crescente.

### Teste de vulnerabilidade

Busca falhas de segurança.

## Caixa-branca e caixa-preta

Caixa-branca usa conhecimento da estrutura interna do código.

Caixa-preta avalia entradas, saídas e comportamento, sem considerar implementação.

Exemplo:

- caixa-branca: cobrir todos os ramos de uma função;
- caixa-preta: testar se login falha com senha incorreta.

## Regressão e automação

Teste de regressão verifica se mudanças novas quebraram comportamento antigo.

Automação permite executar testes repetidamente com baixo custo manual.

Ponto de prova: automação não elimina necessidade de planejamento de teste.

## Refatoração, débito técnico e code smells

Refatoração melhora estrutura interna sem alterar comportamento externo.

Débito técnico é o custo futuro de uma solução tomada por pressa, desconhecimento ou restrição.

Code smell é indício de problema.

Exemplos:

- método muito longo;
- classe com responsabilidades demais;
- duplicação;
- muitos parâmetros;
- nomes ruins;
- alto acoplamento.

## Métricas de código

Métricas ajudam a identificar risco.

Exemplos:

- complexidade ciclomática;
- cobertura de testes;
- duplicação;
- acoplamento;
- coesão;
- tamanho de classe/método;
- taxa de defeitos.

Métrica não deve ser usada isoladamente. Cobertura alta não garante bons testes.

## Auditoria de sistemas

Auditoria avalia controles, riscos, conformidade, rastreabilidade e integridade.

Pode verificar:

- logs;
- trilhas de auditoria;
- segregação de funções;
- perfis de acesso;
- integridade de dados;
- conformidade com políticas;
- controles de mudança.

## Estruturas de dados

Estrutura de dados organiza informações para acesso e manipulação eficientes.

### Vetor e matriz

Vetor é sequência indexada.

Matriz é estrutura bidimensional.

Vantagem: acesso direto por índice.

Desvantagem: inserções e remoções no meio podem ser custosas.

### Lista encadeada

Cada elemento aponta para o próximo.

Vantagem: inserção e remoção flexíveis.

Desvantagem: acesso sequencial, sem índice direto eficiente.

### Pilha

Política LIFO: último a entrar, primeiro a sair.

Operações:

- push;
- pop;
- top/peek.

Exemplos:

- desfazer ação;
- chamada de funções;
- avaliação de expressões.

### Fila

Política FIFO: primeiro a entrar, primeiro a sair.

Operações:

- enqueue;
- dequeue.

Exemplos:

- impressão;
- processamento de mensagens;
- atendimento por ordem de chegada.

### Heap

Estrutura que mantém elemento prioritário no topo.

Usada em:

- filas de prioridade;
- algoritmos de grafos;
- ordenação heapsort.

### Árvores

Árvore é estrutura hierárquica.

Conceitos:

- raiz;
- nó;
- folha;
- altura;
- nível;
- subárvore.

Árvore binária: cada nó tem no máximo dois filhos.

Árvore binária de busca: valores menores à esquerda, maiores à direita.

AVL: árvore binária de busca autobalanceada.

Árvores B e B+ são comuns em bancos de dados e sistemas de arquivos por reduzirem acessos a disco.

## Algoritmos

Algoritmo é sequência finita de passos para resolver um problema.

## Busca

### Busca linear

Percorre elementos um por um.

Complexidade: O(n).

Funciona com dados desordenados.

### Busca binária

Divide o espaço de busca ao meio.

Pré-condição: dados ordenados.

Complexidade: O(log n).

## Ordenação

### Bubble sort

Simples, mas ineficiente.

Complexidade média: O(n²).

### Selection sort

Seleciona menor elemento e posiciona.

Complexidade: O(n²).

### Insertion sort

Eficiente para pequenas entradas ou dados quase ordenados.

Complexidade média: O(n²).

### Merge sort

Divide e conquista.

Complexidade: O(n log n).

### Quick sort

Usa pivô e particionamento.

Complexidade média: O(n log n). Pior caso: O(n²).

## Complexidade

Complexidade analisa crescimento de custo conforme a entrada aumenta.

Ordem comum:

| Notação | Interpretação |
| --- | --- |
| O(1) | constante |
| O(log n) | logarítmica |
| O(n) | linear |
| O(n log n) | linearítmica |
| O(n²) | quadrática |
| O(2^n) | exponencial |

## Recursão

Recursão ocorre quando função chama a si mesma.

Precisa de:

- caso base;
- redução do problema;
- combinação do resultado.

Erro comum: ausência de caso base gera recursão infinita.

## Grafos e caminho mínimo

Grafo tem vértices e arestas.

Pode ser:

- dirigido ou não dirigido;
- ponderado ou não ponderado;
- cíclico ou acíclico.

Caminho mínimo busca rota de menor custo.

Algoritmos conhecidos:

- Dijkstra: pesos não negativos;
- Bellman-Ford: aceita pesos negativos, mas detecta ciclos negativos;
- Floyd-Warshall: caminhos mínimos entre todos os pares.

## Questões de treino

1. Qual é a diferença entre garantia da qualidade e controle da qualidade?
2. Teste unitário deve depender de banco de dados real?
3. O que é teste de regressão?
4. O que é refatoração?
5. O que é code smell?
6. Pilha usa FIFO ou LIFO?
7. Fila usa FIFO ou LIFO?
8. Busca binária exige qual condição?
9. O que Big O mede?
10. Qual é o risco de recursão sem caso base?

## Gabarito comentado

1. Garantia previne defeitos por processo; controle verifica produto.
2. Em geral, não. Deve ser isolado e rápido.
3. Teste para verificar se mudanças quebraram comportamentos existentes.
4. Melhorar estrutura interna sem mudar comportamento observável.
5. Sinal de possível problema de design, legibilidade ou manutenção.
6. LIFO.
7. FIFO.
8. Dados ordenados.
9. Crescimento do custo conforme aumenta a entrada.
10. Recursão infinita e estouro de pilha.

