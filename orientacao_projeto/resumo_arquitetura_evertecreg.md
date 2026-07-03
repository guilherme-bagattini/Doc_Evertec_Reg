# Resumo da arquitetura e monitoramento do EvertecReg

Os dois diagramas novos complementam os PDFs funcionais com uma visao de infraestrutura, integracoes e observabilidade.

## O que os diagramas mostram

- Uso de Kubernetes, Argo CD, Kafka, Redis, PostgreSQL, Azure Storage e cache.
- Protecao por Firewall, App Gateway e WAF na infraestrutura do cliente.
- Keycloak para autenticacao e emissao de tokens.
- Vault como principal gerenciador de configuracoes e secrets.
- Prometheus e Loki para observabilidade.
- Escalabilidade e fine tuning com KEDA.

## Fluxos e dominios adicionados

- Ambiente de IA com BFF, API, front de manutencao, front de chat e validacao de impacto.
- Consulta de documentos para RAG a partir de Confluence, Git e arquivos.
- Regeracao recorrente do banco vetorial e atualizacao do RAG.
- Publicacao e consumo de eventos em Kafka para impacto, monitoramento e logs.
- Acesso a base do cliente via MCP protegido por WAF/App Gateway.

## Leitura pratica

Esses diagramas indicam que o projeto nao e apenas um produto funcional, mas uma plataforma com varias camadas:

1. aplicacao e frontend;
2. mensageria e processamento assincrono;
3. configuracao e seguranca;
4. observabilidade e auditoria;
5. motor de IA e RAG;
6. integracao com bases e documentos do cliente.

## Como usar este material

- Consulte este resumo quando a duvida for sobre infraestrutura, integracoes e monitoramento.
- Consulte o [resumo de requisitos](resumo_pdfs_evertecreg.md) quando a duvida for sobre regras de negocio, telas e fluxos de produto.