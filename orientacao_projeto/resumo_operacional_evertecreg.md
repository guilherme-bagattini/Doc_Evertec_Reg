# Resumo operacional do EvertecReg

Este arquivo e a versao mais objetiva para consulta diaria.

## 1. O que o produto faz

- Captura informacoes regulatorias relevantes.
- Filtra e classifica o que importa para cada cliente, modulo, area ou produto.
- Analisa impacto regulatorio com apoio de IA e regras do negocio.
- Distribui tarefas e informacoes para execucao em ferramentas como Jira e Teams.
- Registra evidencias, logs, auditoria e historico.

## 2. O que precisa ser validado

- O que entra no MVP e o que fica para depois.
- Quais integrações ja estao confirmadas.
- Qual o nivel minimo de detalhamento exigido em logs e auditoria.
- Como fica a governanca de fontes, reguladores e execucoes por cliente.
- Quais fontes alimentam a IA e quais sao apenas referenciais.

## 3. O que depende de arquitetura e integracoes

- Kafka para eventos e troca de mensagens.
- PostgreSQL para dados transacionais.
- Redis para cache.
- Vault para secrets e configuracoes.
- Keycloak para autenticacao.
- Kubernetes, Argo CD e KEDA para deploy e escala.
- Prometheus e Loki para observabilidade.
- WAF e App Gateway para protecao de borda.

## Regra de leitura rapida

Se a duvida for sobre algo novo, pergunte primeiro:

1. isso e produto, validacao ou arquitetura?
2. isso altera o que o cliente ve ou apenas a operacao interna?
3. isso gera evidencias, logs ou mudanca de configuracao?

Essa triagem normalmente reduz ruido e ajuda a localizar o documento certo mais rapido.