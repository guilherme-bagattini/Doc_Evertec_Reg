# Desenvolvimento do EvertecReg - Versao estruturada

Fonte principal: [Desenvolvimento do EvertecReg.pdf](Desenvolvimento%20do%20EvertecReg.pdf)

## Objetivo deste arquivo

Transformar o conteudo do PDF em leitura operacional para acompanhamento de produto, UX e desenvolvimento.

## Mapa por blocos

## 1. Fundacao tecnica e arquitetura

- Fundacao de infraestrutura com Kubernetes, Argo CD, Kafka/Event Hubs, PostgreSQL, Redis, Vault e observabilidade.
- Regras de modelagem com separacao entre dados brutos, classificados e curados.
- Regra estruturante recorrente: nao sobrescrever dados sem versionamento e manter rastreabilidade completa.

IDs e referencias encontradas:

- SQFUNDOS-41062 (modelagem de dados)
- SQFUNDOS-40704 (infraestrutura)
- SD-261817 (relacao com modelagem)

## 2. Web scraping e coleta

- Coleta automatizada de publicacoes em reguladores/autoreguladores.
- Persistencia inicial de dados brutos (HTML, PDF, metadados e status).
- Retry automatico e registro de logs por execucao.

IDs e referencias encontradas:

- SQFUNDOS-42167 (historia de scraping)
- SQFUNDOS-41058 (epico de scraping)

## 3. Configuracoes administrativas

- Modulos, empresas, execucoes, reguladores e fontes.
- Edicoes com confirmacao explicita e impacto apenas em execucoes futuras.
- Regras de descarte automatico por fonte.

IDs e referencias encontradas:

- SQFUNDOS-42160 (epico tela configuracoes)
- SQFUNDOS-42161 (modulos)
- SQFUNDOS-42162 (empresas)
- SQFUNDOS-42168 (execucoes)
- SQFUNDOS-42169 (regulador e fontes)

## 4. Curadoria

- Operador interno revisa publicacoes coletadas antes de disponibilizar ao cliente.
- Acoes principais: editar, gravar estado intermediario, aprovar, descartar com justificativa obrigatoria.
- Publicacoes curadas nao devem ser reavaliadas nesta tela; consulta posterior em logs.

IDs e referencias encontradas:

- SQFUNDOS-42504 (epico curadoria)
- SQFUNDOS-42507 (relacao com consulta/logs)

## 5. Consulta e logs

- Visao tecnica de execucoes e historico de publicacoes.
- Filtros por data, regulador, fonte e status.
- Tela estritamente consultiva para auditoria e suporte.

IDs e referencias encontradas:

- SQFUNDOS-42504 (epico logs e execucoes)
- SQFUNDOS-42494, SQFUNDOS-42496, SD-267482 (dashboard e dominio relacionado)

## 6. Configuracoes do cliente (dominio seguinte)

- Cadastro e gestao de produtos, areas, colaboradores, documentacao, integracoes e regras de negocio.
- Escopo por company_id (multitenancy).
- IA com pertinencia por area e impacto por produto.

IDs e referencias encontradas:

- SD-269875
- SQFUNDOS-43084
- SQFUNDOS-43085
- SQFUNDOS-43094

## 7. Itens pos-MVP explicitados

- Dashboard ampliado.
- Portfolios.
- Cadastro em bloco avancado (clientes).
- Chatbot com IA.

## Gaps recorrentes para acompanhamento

- Versionamento: regra forte no documento, mas com alinhamentos de etapa indicando simplificacao no MVP.
- Permissoes: papeis existem, mas matriz fina por acao precisa fechar.
- Erros: status generico na UI exige boa taxonomia de logs para operacao.
- Reversao de aprovacao: fluxo precisa definicao formal (sistemico ou operacional).

## Como usar junto com o tracker

1. Use este arquivo para entender o contexto por epico e dominio.
2. Use [acompanhamento_desenvolvimento_evertecreg.csv](acompanhamento_desenvolvimento_evertecreg.csv) para acompanhamento de acao, dono e status.
