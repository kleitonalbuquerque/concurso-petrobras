# Arquitetura de Aplicações e Linguagens

## Arquitetura de aplicações

Arquitetura define a organização de alto nível de um sistema: componentes, responsabilidades, comunicação, decisões técnicas e restrições.

Uma boa arquitetura busca:

- baixo acoplamento;
- alta coesão;
- manutenibilidade;
- escalabilidade;
- segurança;
- testabilidade;
- observabilidade.

## MVC

MVC separa a aplicação em:

- Model: regras de negócio e dados;
- View: interface ou representação visual;
- Controller: coordena entrada, fluxo e interação.

Objetivo: separar responsabilidades. A interface não deve concentrar regra de negócio.

Ponto de prova: MVC não é o mesmo que arquitetura em camadas, embora possa ser combinado com ela.

## Arquitetura em N camadas

Divide o sistema em camadas lógicas.

Exemplo comum:

- apresentação;
- aplicação;
- domínio/negócio;
- persistência;
- banco de dados.

Vantagens:

- organização;
- reutilização;
- separação de responsabilidades;
- facilidade de manutenção.

Risco: excesso de camadas pode gerar complexidade e latência.

## SOA e ESB

SOA é arquitetura orientada a serviços. Funcionalidades são expostas como serviços reutilizáveis.

Características:

- interoperabilidade;
- contratos de serviço;
- reuso;
- baixo acoplamento;
- composição de serviços.

ESB é barramento de serviços corporativos. Atua como mediador entre sistemas.

Funções do ESB:

- roteamento;
- transformação de mensagens;
- orquestração;
- mediação;
- integração com sistemas legados.

Ponto de prova: ESB pode virar gargalo se concentrar lógica e tráfego demais.

## Microsserviços

Microsserviços dividem o sistema em serviços pequenos, independentes e orientados a capacidades de negócio.

Características:

- deploy independente;
- banco de dados preferencialmente independente por serviço;
- comunicação via APIs ou eventos;
- autonomia de times;
- observabilidade forte.

Vantagens:

- escalabilidade granular;
- autonomia;
- isolamento de falhas;
- evolução independente.

Desvantagens:

- complexidade operacional;
- comunicação distribuída;
- consistência eventual;
- monitoramento mais difícil;
- testes de integração mais complexos.

Ponto de prova: microsserviços não são solução universal. Para sistemas simples, monólito modular pode ser melhor.

## Arquitetura orientada a eventos

Nessa arquitetura, componentes reagem a eventos.

Evento é um fato ocorrido:

- pedido criado;
- pagamento aprovado;
- sensor mediu temperatura;
- usuário alterou cadastro.

Vantagens:

- desacoplamento;
- processamento assíncrono;
- escalabilidade;
- integração entre sistemas.

Riscos:

- rastreabilidade mais difícil;
- ordem de eventos;
- duplicidade;
- consistência eventual.

## Mensageria e publish-subscribe

Mensageria permite comunicação por mensagens, geralmente assíncrona.

Fila:

- um produtor envia;
- um consumidor processa;
- cada mensagem normalmente é consumida uma vez.

Tópico publish-subscribe:

- produtor publica;
- vários consumidores assinam;
- a mesma mensagem pode ser entregue a múltiplos assinantes.

## REST, JSON, SOAP e XML

REST é estilo arquitetural baseado em recursos. Usa HTTP de forma semântica.

Exemplos:

- GET /usuarios: listar usuários;
- POST /usuarios: criar usuário;
- PUT /usuarios/10: substituir usuário;
- PATCH /usuarios/10: alterar parcialmente;
- DELETE /usuarios/10: remover.

JSON é formato leve baseado em pares chave-valor.

SOAP é protocolo mais formal, geralmente baseado em XML, com contrato WSDL.

XML é linguagem de marcação extensível. É mais verboso que JSON, mas útil em integrações formais.

WSDL descreve serviços SOAP. UDDI é registro para descoberta de serviços.

## API gateway

API gateway é ponto de entrada para APIs.

Pode cuidar de:

- autenticação;
- autorização;
- rate limiting;
- roteamento;
- logs;
- métricas;
- transformação;
- cache.

## Cloud native e contêineres

Aplicação cloud native é projetada para rodar bem em ambientes de nuvem.

Características:

- elasticidade;
- automação;
- resiliência;
- observabilidade;
- deploy frequente;
- contêineres;
- configuração externa;
- serviços gerenciados.

Contêiner empacota aplicação e dependências em uma unidade isolada.

Diferença para VM:

- VM virtualiza hardware;
- contêiner virtualiza ambiente de execução sobre o mesmo kernel.

## Design patterns e anti-patterns

Design pattern é solução recorrente para problema comum.

Exemplos:

- Factory: cria objetos sem expor lógica de criação;
- Singleton: garante instância única;
- Observer: notifica interessados quando estado muda;
- Strategy: troca algoritmo em tempo de execução;
- Adapter: compatibiliza interfaces.

Anti-pattern é solução comum que causa problemas.

Exemplos:

- God Object: objeto concentra responsabilidades demais;
- Spaghetti Code: código sem estrutura clara;
- Golden Hammer: usar a mesma solução para tudo;
- Lava Flow: código morto ou legado que ninguém remove.

## Persistência e ORM

Persistência é armazenamento durável de dados.

ORM mapeia objetos para tabelas relacionais.

Vantagens:

- reduz código repetitivo;
- facilita operações comuns;
- aumenta produtividade.

Riscos:

- consultas ineficientes;
- problema N+1;
- abstração excessiva;
- dificuldade para otimizar SQL.

## Linguagens de programação

### Orientação a objetos

Conceitos:

- classe: molde;
- objeto: instância;
- encapsulamento: proteção de estado interno;
- herança: reaproveitamento por especialização;
- polimorfismo: mesmo contrato, comportamentos diferentes;
- abstração: focar características essenciais.

Ponto de prova: herança aumenta acoplamento. Composição muitas vezes é alternativa mais flexível.

### Coleções e genéricos

Coleções armazenam conjuntos de elementos: listas, mapas, conjuntos, filas.

Genéricos permitem parametrizar tipos.

Exemplo conceitual:

```text
Lista<String>
Lista<Integer>
```

Vantagem: reutilização com segurança de tipo.

### Threads, sincronização e deadlock

Thread é fluxo de execução dentro de processo.

Problemas comuns:

- condição de corrida;
- deadlock;
- starvation;
- inconsistência de dados.

Deadlock ocorre quando tarefas ficam bloqueadas esperando recursos umas das outras.

Condições clássicas:

- exclusão mútua;
- posse e espera;
- não preempção;
- espera circular.

### Garbage collector

Garbage collector libera memória de objetos não mais alcançáveis.

Vantagem: reduz erros manuais de memória.

Custo: pausas, sobrecarga e necessidade de entender ciclo de vida de objetos em aplicações críticas.

### Exceções

Exceções tratam fluxos de erro.

Boas práticas:

- capturar exceções específicas;
- não engolir erro silenciosamente;
- registrar contexto;
- não usar exceção para fluxo normal de negócio.

### HTML, CSS e JavaScript

HTML estrutura o conteúdo.

CSS define apresentação.

JavaScript define comportamento.

Separação:

- HTML: o que existe;
- CSS: como aparece;
- JavaScript: como se comporta.

### Python

Python é linguagem de alto nível, legível e muito usada em automação, dados, APIs e scripts.

Características:

- tipagem dinâmica;
- sintaxe simples;
- bibliotecas abundantes;
- boa para produtividade.

### .NET Core

.NET Core é plataforma moderna, multiplataforma e modular para desenvolvimento com C# e ecossistema .NET.

Usos:

- APIs;
- aplicações web;
- serviços;
- aplicações corporativas.

## Questões de treino

1. MVC e arquitetura em camadas são a mesma coisa?
2. Qual é a função de um ESB?
3. Cite uma vantagem e uma desvantagem de microsserviços.
4. Qual é a diferença entre fila e publish-subscribe?
5. REST é protocolo?
6. SOAP costuma usar qual formato e qual contrato?
7. Para que serve um API gateway?
8. O que é problema N+1 em ORM?
9. Qual é a diferença entre classe e objeto?
10. O que caracteriza deadlock?

## Gabarito comentado

1. Não. MVC separa modelo, visão e controle; camadas separam níveis lógicos da aplicação.
2. Mediar integração entre serviços, com roteamento, transformação e orquestração.
3. Vantagem: deploy independente. Desvantagem: complexidade operacional.
4. Fila tende a entregar para um consumidor; pub-sub entrega a múltiplos assinantes.
5. Não. É um estilo arquitetural.
6. XML e WSDL.
7. Centralizar entrada, segurança, roteamento, limites e observabilidade de APIs.
8. Muitas consultas adicionais geradas ao buscar entidades relacionadas individualmente.
9. Classe é modelo; objeto é instância concreta.
10. Tarefas aguardam recursos entre si e nenhuma progride.

