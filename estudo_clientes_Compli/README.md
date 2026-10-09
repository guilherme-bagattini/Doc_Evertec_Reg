# Estudo com clientes - EvertecReg

Esta pasta reune pesquisa com clientes (entrevistas, transcricoes, sinteses) e os materiais derivados dela (demandas, frameworks, dashboards), sem misturar com a documentacao principal do projeto.

## Indice rapido

| Preciso de... | Vá para |
| --- | --- |
| Perguntas-guia para conduzir uma entrevista | [Perguntas-guia](#perguntas-guia-para-entrevistas) abaixo |
| Modelo em branco para registrar entrevista | [entrevistas/modelo_entrevista.md](entrevistas/modelo_entrevista.md) |
| Lista de entrevistas ja feitas | [Entrevistas realizadas](#entrevistas-realizadas) abaixo |
| Demandas de produto extraidas das entrevistas | [demandas_clientes_entrevistas.md](demandas_clientes_entrevistas.md) |
| Como priorizar as demandas (frameworks) | [frameworks_analise_prioritizacao.md](frameworks_analise_prioritizacao.md) |
| Classificacao de risco/uso por cliente | [sinteses/2026-07-07_classificacao_estrelas_clientes.md](sinteses/2026-07-07_classificacao_estrelas_clientes.md) |
| Plano de retencao/renovacao por conta | [sinteses/plano_reativacao_renovacao_clientes.md](sinteses/plano_reativacao_renovacao_clientes.md) |
| Painel visual de engajamento/churn | [dashboard_clientes.html](dashboard_clientes.html) |
| Analise detalhada de usabilidade e risco de churn | [dashboard_usabilidade_churn.html](dashboard_usabilidade_churn.html) |

## Estrutura

- `entrevistas/`: registros resumidos por cliente ou contato (usar o modelo padrao).
- `transcricoes/`: transcricoes completas ou parciais de reunioes.
- `sinteses/`: consolidacoes, padroes recorrentes, classificacoes e planos de acao.
- Arquivos na raiz: materiais derivados que cruzam varias entrevistas (demandas de produto, frameworks de priorizacao, dashboards).

## Fluxo de uso (da entrevista a ideia acionavel)

1. Fazer a entrevista usando as [perguntas-guia](#perguntas-guia-para-entrevistas).
2. Registrar em `entrevistas/` (modelo em [entrevistas/modelo_entrevista.md](entrevistas/modelo_entrevista.md)) e, se houver gravacao, salvar a integra em `transcricoes/`.
3. Extrair demandas concretas para [demandas_clientes_entrevistas.md](demandas_clientes_entrevistas.md), sempre citando a entrevista de origem.
4. Priorizar usando os frameworks em [frameworks_analise_prioritizacao.md](frameworks_analise_prioritizacao.md).
5. Consolidar aprendizados recorrentes e classificacao de risco/uso em `sinteses/`.
6. Atualizar o painel (`dashboard_clientes.html`) quando houver mudanca relevante de cenario.

## Perguntas-guia para entrevistas

Use como ponto de partida, adaptando conforme o cliente:

- Qual e o objetivo de negocio do cliente com a plataforma?
- Como e o uso hoje (frequencia, modulos usados, quem usa)?
- O que motivou o baixo/alto uso atual?
- Quais dores ou bloqueios impedem o uso pleno?
- O que o cliente espera que a plataforma resolva e ainda nao resolve?
- Ha comparacao com concorrentes ou alternativas (planilhas, outras ferramentas, IA)?
- Qual o risco percebido de cancelamento e por que?
- Qual oportunidade de expansao de uso ou de modulos existe?
- Quais sao os proximos passos combinados e quem e o responsavel?

## Convencao de nomes

- Um arquivo por reuniao ou entrevista.
- Padrao de nome: `AAAA-MM-DD_cliente_tema.md`
- Se houver anonimizacao, usar identificadores como `cliente_01`, `cliente_02`.

## Campos uteis para o registro

- Data
- Cliente ou identificador
- Participantes
- Contexto da conversa
- Principais dores
- Necessidades citadas
- Riscos ou bloqueios
- Oportunidades percebidas
- Proximos passos

## Entrevistas realizadas

| Data | Cliente | Arquivo |
| --- | --- | --- |
| 2026-07-03 | Algarve Investimentos | [entrevistas/2026-07-03_algarve_investimentos_reuniao.md](entrevistas/2026-07-03_algarve_investimentos_reuniao.md) |
| 2026-07-06 | Nivi Capital | [entrevistas/2026-07-06_nivi_capital_reuniao.md](entrevistas/2026-07-06_nivi_capital_reuniao.md) |
| 2026-07-07 | AWR Capital | [entrevistas/2026-07-07_awr_capital_reuniao.md](entrevistas/2026-07-07_awr_capital_reuniao.md) |
| 2026-07-07 | Hike Capital | [entrevistas/2026-07-07_hike_capital_reuniao.md](entrevistas/2026-07-07_hike_capital_reuniao.md) |
| 2026-07-08 | Capsicum Assets | [entrevistas/2026-07-08_capsicum_assets_reuniao.md](entrevistas/2026-07-08_capsicum_assets_reuniao.md) |
| 2026-07-10 | Daemon Investments | [entrevistas/2026-07-10_daemon_reuniao.md](entrevistas/2026-07-10_daemon_reuniao.md) |
| 2026-07-13 | Casaforte Investimentos | [entrevistas/2026-07-13_casaforte_investimentos_reuniao.md](entrevistas/2026-07-13_casaforte_investimentos_reuniao.md) |
| 2026-07-14 | Agro Eldorado | [entrevistas/2026-07-14_agro_eldorado_reuniao.md](entrevistas/2026-07-14_agro_eldorado_reuniao.md) |
| 2026-07-15 | Alaska | [entrevistas/2026-07-15_alaska_reuniao.md](entrevistas/2026-07-15_alaska_reuniao.md) |
| 2026-08-04 | Prada | [entrevistas/2026-08-04_prada_reuniao.md](entrevistas/2026-08-04_prada_reuniao.md) |
| 2026-08-07 | SVN Gestao | [entrevistas/2026-08-07_svn_reuniao.md](entrevistas/2026-08-07_svn_reuniao.md) |
| 2026-08-10 | Gera Capital | [entrevistas/2026-08-10_gera_reuniao.md](entrevistas/2026-08-10_gera_reuniao.md) |

## Observacao

Se quiser, depois eu posso deixar isso mais estruturado com modelos padrao para entrevista e para transcricao.