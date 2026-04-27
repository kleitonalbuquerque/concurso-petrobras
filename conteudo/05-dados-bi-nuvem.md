# Arquitetura de Dados, BI, Big Data e Nuvem

## Modelagem de dados

Modelagem de dados representa entidades, atributos, relacionamentos e regras de um domínio.

### Modelo conceitual

Visão de alto nível, independente de tecnologia.

Responde:

- quais entidades existem?
- como se relacionam?
- quais regras principais importam?

### Modelo lógico

Representa estrutura adaptada a um paradigma, como relacional.

Define:

- tabelas;
- colunas;
- chaves;
- relacionamentos;
- cardinalidade.

### Modelo físico

Detalha implementação no SGBD.

Inclui:

- tipos de dados;
- índices;
- particionamento;
- constraints;
- tablespaces;
- estratégias de armazenamento.

## DER

Diagrama entidade-relacionamento mostra entidades, atributos e relacionamentos.

Conceitos:

- entidade: objeto do domínio;
- atributo: característica;
- relacionamento: associação;
- cardinalidade: quantidade de ocorrências relacionadas.

Exemplo:

> Cliente realiza Pedido.

Um cliente pode realizar vários pedidos; um pedido pertence a um cliente.

## Normalização

Normalização reduz redundância e anomalias.

### Primeira forma normal

Evita grupos repetitivos e atributos multivalorados.

### Segunda forma normal

Remove dependências parciais em chave composta.

### Terceira forma normal

Remove dependências transitivas.

Ponto de prova: normalização favorece consistência, mas pode exigir mais joins.

## Integridade referencial

Garante que chave estrangeira aponte para registro existente.

Exemplo:

Um pedido com `cliente_id = 10` só é válido se existir cliente com id 10.

## SQL, DDL e DML

SQL é linguagem para manipular e consultar bancos relacionais.

DDL define estrutura:

- CREATE;
- ALTER;
- DROP;
- TRUNCATE.

DML manipula dados:

- INSERT;
- UPDATE;
- DELETE;
- SELECT, em muitos materiais.

## ACID

ACID descreve propriedades de transações.

Atomicidade: tudo ou nada.

Consistência: transação leva banco de um estado válido a outro.

Isolamento: transações concorrentes não interferem indevidamente.

Durabilidade: após commit, o resultado persiste.

## Transações e isolamento

Problemas de concorrência:

- dirty read: ler dado não confirmado;
- non-repeatable read: mesma consulta retorna valor diferente;
- phantom read: nova linha aparece em consulta repetida;
- lost update: atualização de uma transação sobrescreve outra.

Níveis comuns:

- Read Uncommitted;
- Read Committed;
- Repeatable Read;
- Serializable.

## Performance de banco

Fatores importantes:

- índices adequados;
- consultas seletivas;
- estatísticas atualizadas;
- normalização/desnormalização consciente;
- particionamento;
- análise de plano de execução.

Índice acelera leitura, mas pode aumentar custo de escrita.

## NoSQL

NoSQL agrupa bancos não relacionais.

Tipos:

- chave-valor;
- documentos;
- colunas;
- grafos.

Usos:

- escala horizontal;
- flexibilidade de esquema;
- baixa latência;
- dados semiestruturados;
- relacionamentos complexos, no caso de grafos.

## Metadados e dados mestres

Metadados são dados sobre dados.

Exemplos:

- origem;
- tipo;
- dono;
- sensibilidade;
- qualidade;
- regra de negócio.

Dados mestres representam entidades centrais, como cliente, produto, fornecedor.

Dados de referência são listas padronizadas, como país, estado, categoria.

## ETL e integração de dados

ETL:

- Extract: extrair;
- Transform: transformar;
- Load: carregar.

ELT carrega antes e transforma no destino, comum em ambientes modernos de dados.

Integração pode ocorrer por:

- arquivos;
- APIs;
- mensageria;
- replicação;
- acesso a base de dados;
- pipelines.

## Data warehouse, OLAP e BI

Data warehouse é repositório orientado a análise, integrado, histórico e organizado para decisão.

OLAP permite análise multidimensional.

Operações:

- drill-down: detalhar;
- roll-up: agregar;
- slice: filtrar uma dimensão;
- dice: combinar filtros;
- pivot: mudar perspectiva.

BI transforma dados em informações para decisão.

## Modelagem dimensional

Usa fatos e dimensões.

Tabela fato:

- contém métricas;
- possui chaves para dimensões.

Dimensões:

- tempo;
- produto;
- cliente;
- local;
- canal.

Esquemas:

- estrela: dimensões ligadas diretamente ao fato;
- floco de neve: dimensões normalizadas.

## Dashboards e relatórios

Relatório detalha dados.

Dashboard monitora indicadores.

Bom dashboard:

- mostra poucos indicadores relevantes;
- deixa claro o período;
- evita excesso visual;
- permite comparação;
- indica tendência e alerta.

## Data lake e Big Data

Data lake armazena dados em formatos variados, brutos ou tratados.

Big Data costuma ser associado aos Vs:

- volume;
- velocidade;
- variedade;
- veracidade;
- valor.

## Computação em nuvem

Nuvem oferece recursos computacionais sob demanda, com pagamento conforme uso e provisionamento automatizado.

### Modelos de serviço

IaaS: infraestrutura como serviço. Exemplo: máquinas virtuais, redes, discos.

PaaS: plataforma como serviço. Exemplo: banco gerenciado, runtime de aplicação.

SaaS: software como serviço. Exemplo: e-mail corporativo, CRM.

### Benefícios

- elasticidade;
- escalabilidade;
- alta disponibilidade;
- agilidade;
- recuperação de desastres;
- redução de investimento inicial;
- automação.

### Região e zona de disponibilidade

Região é localização geográfica.

Zona de disponibilidade é área isolada dentro de uma região.

Usar múltiplas zonas aumenta resiliência.

### Segurança e responsabilidade compartilhada

Na nuvem, segurança é compartilhada.

Provedor cuida da segurança da nuvem.

Cliente cuida da segurança no uso da nuvem:

- identidades;
- permissões;
- dados;
- configurações;
- aplicações.

### Custos

Custos dependem de:

- computação;
- armazenamento;
- transferência de dados;
- licenças;
- tempo ligado;
- nível de serviço.

Boas práticas:

- desligar recursos ociosos;
- dimensionar corretamente;
- usar tags;
- monitorar consumo;
- reservar capacidade quando fizer sentido.

## IoT

IoT conecta dispositivos físicos capazes de coletar, enviar ou receber dados.

Componentes:

- sensores;
- atuadores;
- conectividade;
- gateway;
- plataforma;
- análise.

Desafios:

- segurança;
- escala;
- atualização;
- energia;
- conectividade instável.

## Infrastructure as Code

IaC gerencia infraestrutura por arquivos versionáveis.

Benefícios:

- repetibilidade;
- auditoria;
- automação;
- redução de erro manual;
- revisão por pares;
- rollback.

Exemplos conceituais:

- declarar rede;
- declarar banco;
- declarar permissões;
- declarar ambiente.

## Questões de treino

1. Qual é a diferença entre modelo conceitual, lógico e físico?
2. Para que serve normalização?
3. O que é integridade referencial?
4. Quais são as propriedades ACID?
5. Índice sempre melhora performance?
6. Quando NoSQL pode ser adequado?
7. O que é tabela fato?
8. Qual é a diferença entre relatório e dashboard?
9. O que significa responsabilidade compartilhada em nuvem?
10. Qual é a vantagem de IaC?

## Gabarito comentado

1. Conceitual é alto nível; lógico estrutura o modelo; físico detalha implementação.
2. Reduzir redundância e anomalias.
3. Garantir que chaves estrangeiras apontem para registros existentes.
4. Atomicidade, consistência, isolamento e durabilidade.
5. Não. Ajuda leituras, mas pode prejudicar escritas e ocupar espaço.
6. Quando há escala, flexibilidade de esquema ou modelos não relacionais.
7. Tabela com métricas e chaves para dimensões.
8. Relatório detalha; dashboard monitora indicadores.
9. Provedor e cliente dividem responsabilidades de segurança.
10. Tornar infraestrutura repetível, versionável e automatizável.

