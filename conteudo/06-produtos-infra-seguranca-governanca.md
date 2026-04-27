# Produtos, Infraestrutura, Segurança e Governança

## Gerenciamento de produtos de software

Produto de software não é apenas um projeto. Produto é algo que entrega valor contínuo para usuários e para a organização.

Gestão de produto envolve:

- entender problemas;
- priorizar valor;
- definir visão;
- organizar backlog;
- medir resultados;
- ajustar estratégia.

## Scrum no produto

Scrum ajuda a entregar valor em ciclos curtos.

Pontos importantes:

- Product Owner prioriza o Product Backlog;
- Sprint gera incremento;
- Review coleta feedback;
- Retrospective melhora o processo.

Erro comum: achar que Product Owner é gerente de equipe. Ele gerencia valor e prioridade do produto.

## Kanban no produto

Kanban ajuda a visualizar fluxo de trabalho.

Conceitos:

- quadro;
- colunas;
- cartões;
- limite de WIP;
- lead time;
- throughput.

Usado quando o trabalho é contínuo, com demandas chegando em fluxo.

## SAFe e portfólio

SAFe é framework para agilidade em escala.

Busca alinhar:

- times;
- programas;
- portfólio;
- estratégia;
- governança.

Ponto de prova: SAFe não é apenas Scrum grande. Ele adiciona camadas de coordenação e planejamento.

## Dado, informação, conhecimento e inteligência

Dado: registro bruto.

Informação: dado interpretado em contexto.

Conhecimento: capacidade de agir ou decidir com base em informação e experiência.

Inteligência: uso estratégico do conhecimento para orientar decisão.

Exemplo:

- dado: 120 ms;
- informação: tempo médio de resposta foi 120 ms;
- conhecimento: está dentro do SLA;
- inteligência: podemos manter a arquitetura atual por enquanto.

## Dados estruturados e não estruturados

Estruturados:

- tabelas;
- colunas;
- tipos definidos;
- SQL.

Não estruturados:

- textos;
- imagens;
- PDFs;
- áudios;
- logs livres.

Semiestruturados:

- JSON;
- XML;
- YAML.

## Planilhas

Planilhas são úteis para análise simples, mas têm riscos:

- erro manual;
- falta de controle de versão;
- duplicidade;
- fórmulas ocultas;
- dificuldade de auditoria.

Boas práticas:

- separar entrada, cálculo e saída;
- proteger células críticas;
- documentar fórmulas;
- validar dados;
- evitar planilha como sistema permanente.

## Infraestrutura computacional

Infraestrutura inclui recursos que sustentam sistemas:

- servidores;
- redes;
- armazenamento;
- sistemas operacionais;
- virtualização;
- filas;
- processos;
- monitoramento.

## Processamento paralelo e distribuído

Paralelo: várias tarefas executam ao mesmo tempo, geralmente para acelerar processamento.

Distribuído: componentes em máquinas diferentes cooperam por rede.

Desafios:

- sincronização;
- falhas parciais;
- latência;
- consistência;
- particionamento.

## HPC

High Performance Computing é computação de alto desempenho.

Usos:

- simulações;
- processamento científico;
- modelos complexos;
- grandes volumes de cálculo.

## Virtualização

Virtualização cria recursos lógicos a partir de recursos físicos.

Tipos:

- computação: máquinas virtuais;
- armazenamento: volumes lógicos;
- rede: redes virtuais, VLANs, SDN.

Vantagens:

- melhor uso de recursos;
- isolamento;
- provisionamento rápido;
- recuperação mais simples.

## Protocolos

TCP/IP: base de comunicação da internet.

HTTP: protocolo de aplicação para web.

HTTPS: HTTP com TLS.

FTP: transferência de arquivos.

SMTP: envio de e-mails.

LDAP: acesso a diretórios.

SSL/TLS: segurança de transporte.

SAML: federação de identidade e SSO.

OAuth: autorização delegada.

Ponto de prova: OAuth não é protocolo de autenticação puro; ele trata principalmente de autorização delegada.

## Segurança da informação

Segurança busca proteger:

- confidencialidade;
- integridade;
- disponibilidade.

Também envolve autenticidade, não repúdio, rastreabilidade e conformidade.

## Segurança física e lógica

Física:

- controle de acesso a salas;
- energia;
- climatização;
- proteção contra incêndio;
- câmeras;
- racks.

Lógica:

- autenticação;
- autorização;
- criptografia;
- logs;
- firewalls;
- hardening;
- políticas.

## Operação de segurança

Envolve monitorar, detectar, responder e recuperar.

Ferramentas:

- firewall;
- proxy;
- IDS/IPS;
- DLP;
- CASB;
- SIEM;
- antivírus;
- EDR;
- WAF.

Resumo:

- IDS detecta;
- IPS bloqueia;
- SIEM correlaciona logs;
- EDR atua em endpoints;
- WAF protege aplicações web;
- DLP previne vazamento de dados;
- CASB controla uso de serviços em nuvem.

## Malwares e ataques

Malware é software malicioso.

Tipos:

- vírus;
- worm;
- ransomware;
- spyware;
- rootkit;
- trojan.

Ataques web:

- SQL Injection: injeção de comandos SQL;
- XSS: execução de script no navegador da vítima;
- CSRF: uso indevido de sessão autenticada;
- Path Traversal: acesso indevido a caminhos de arquivos;
- DDoS: indisponibilidade por excesso de tráfego.

## Desenvolvimento seguro

Práticas:

- validação de entrada;
- controle de acesso;
- uso de criptografia adequada;
- tratamento seguro de erros;
- gestão de segredos;
- atualização de dependências;
- revisão de código;
- testes de segurança.

SAST: analisa código.

DAST: testa aplicação em execução.

IAST: combina instrumentação e execução.

## Identidade e acesso

Autenticação: provar quem é.

Autorização: definir o que pode fazer.

SSO: login único.

MFA: múltiplos fatores de autenticação.

IAM: gestão de identidades e acessos.

RBAC: permissões por papéis.

ABAC: permissões por atributos.

## Resposta a incidente

NIST SP 800-61 organiza resposta a incidentes em fases:

- preparação;
- detecção e análise;
- contenção, erradicação e recuperação;
- atividade pós-incidente.

Ponto de prova: resposta a incidente não começa quando o ataque ocorre. Começa na preparação.

## Threat intelligence e threat hunting

Threat intelligence usa informações sobre ameaças, atores, técnicas e indicadores.

Threat hunting é busca proativa por sinais de comprometimento ainda não detectados.

## Pentest, STRIDE e MITRE ATT&CK

Pentest simula ataques para identificar vulnerabilidades exploráveis.

STRIDE classifica ameaças:

- Spoofing;
- Tampering;
- Repudiation;
- Information Disclosure;
- Denial of Service;
- Elevation of Privilege.

MITRE ATT&CK organiza táticas e técnicas usadas por adversários reais.

## Riscos, continuidade e normas

ISO 31000: gestão de riscos.

ISO 22301: continuidade de negócios.

ISO 27002: controles de segurança da informação.

SOX: controles e confiabilidade de informações financeiras.

## Criptografia e assinatura digital

Criptografia simétrica usa a mesma chave para cifrar e decifrar.

Criptografia assimétrica usa par de chaves pública e privada.

Hash gera resumo fixo de dados.

Assinatura digital garante:

- autenticidade;
- integridade;
- não repúdio.

Certificado digital liga identidade a chave pública.

## Governança de TI

Governança de TI define estruturas para alinhar TI ao negócio, gerar valor, controlar riscos e medir desempenho.

Objetivos:

- alinhamento estratégico;
- entrega de valor;
- gestão de riscos;
- gestão de recursos;
- mensuração de desempenho.

## ITIL 4

ITIL 4 é referência para gestão de serviços de TI.

Conceitos:

- serviço;
- valor;
- práticas;
- sistema de valor de serviço;
- cadeia de valor de serviço;
- melhoria contínua.

Foco: cocriar valor por meio de serviços.

## Governança de dados e DAMA-DMBoK

Governança de dados define direitos, responsabilidades, políticas e controles sobre dados.

DAMA-DMBoK organiza áreas como:

- arquitetura de dados;
- modelagem;
- qualidade;
- metadados;
- dados mestres;
- segurança;
- integração;
- data warehouse e BI.

## ERP

ERP integra processos corporativos.

Exemplos de módulos:

- finanças;
- compras;
- estoque;
- vendas;
- produção;
- RH.

Vantagem: integração e padronização.

Risco: implantação complexa e dependência de processos bem definidos.

## Questões de treino

1. Qual é a diferença entre Scrum e Kanban?
2. O que é WIP?
3. Qual é a diferença entre dado e informação?
4. Qual é o risco de usar planilha como sistema permanente?
5. Qual é a diferença entre processamento paralelo e distribuído?
6. HTTPS adiciona o quê ao HTTP?
7. IDS e IPS fazem a mesma coisa?
8. O que é SQL Injection?
9. Qual é a diferença entre autenticação e autorização?
10. Quais são as fases gerais de resposta a incidente segundo NIST SP 800-61?
11. O que é STRIDE?
12. ITIL 4 é focado em quê?

## Gabarito comentado

1. Scrum usa sprints e papéis; Kanban foca fluxo contínuo e limite de WIP.
2. Work in Progress, trabalho em andamento.
3. Dado é bruto; informação é dado em contexto.
4. Erro manual, baixa rastreabilidade, falta de controle e dificuldade de auditoria.
5. Paralelo executa simultaneamente; distribuído coordena componentes em máquinas diferentes.
6. Criptografia e autenticação via TLS.
7. Não. IDS detecta; IPS pode bloquear.
8. Injeção de comandos SQL por entradas mal tratadas.
9. Autenticação prova identidade; autorização define permissões.
10. Preparação; detecção/análise; contenção/erradicação/recuperação; pós-incidente.
11. Modelo de classificação de ameaças.
12. Gestão de serviços de TI e cocriação de valor.

