# Guia de reuniao para PO - EvertecReg

Este guia foi feito para apoiar participacao em reunioes do EvertecReg sem depender de contexto tecnico profundo.

## 1) O que o EvertecReg faz

O EvertecReg e a frente de inteligencia regulatoria da suite Compliasset. Ele transforma mudancas regulatórias em acao operacional.

Fluxo simplificado:

1. captura conteudos e normativos em fontes reguladoras;
2. filtra o que e relevante para cliente, area e produto;
3. analisa impacto com apoio de IA e regras de negocio;
4. distribui informacoes e tarefas para execucao (ex.: Jira e Teams);
5. registra logs, evidencias e trilha de auditoria.

Mensagem-chave para reuniao:

- nao e so leitura de norma;
- e operacao com rastreabilidade.

## 2) Termos que vao aparecer na reuniao

- Curadoria: etapa humana de revisao/decisao sobre o que foi coletado.
- Crawling/Scraping: coleta automatica de informacoes em fontes externas.
- IA/RAG: uso de contexto documental para melhorar classificacao e relevancia.
- Gravar x Aprovar: duas etapas de confirmacao para reduzir erro operacional.
- Logs: detalhamento tecnico de sucesso/falha para auditoria e suporte.
- MVP: primeira entrega com escopo mais conservador.
- Incremento pos-MVP: evolucoes planejadas para etapas seguintes.
- KANBAN/cards: formato de distribuicao de demanda no fluxo operacional do cliente.

## 3) Perguntas prontas para quando algo ficar confuso

Use estas perguntas em reuniao para destravar decisoes:

1. Isso esta no MVP ou no pos-MVP?
2. Essa regra e de produto, operacao interna ou arquitetura?
3. Qual evidencia/log comprova que esse fluxo funcionou?
4. Em caso de erro, o que aparece para o usuario e o que fica so no log?
5. Essa decisao depende de dados do cliente ou e regra global?
6. Existe impacto em permissao/perfil de acesso?
7. Essa etapa exige justificativa obrigatoria ou apenas registro simples?
8. O resultado vai para qual canal: tela, Jira, Teams ou outro?
9. O que pode ser alterado agora sem impactar execucoes em andamento?
10. Qual time dono fecha essa decisao: produto, dados, arquitetura ou operacao?

## Atalho de uso antes da reuniao (2 minutos)

1. leia o [Resumo operacional do projeto](resumo_operacional_evertecreg.md);
2. confira [Decisões fechadas para o MVP](decisoes_mvp_evertecreg.md);
3. revise [Dúvidas e decisões em aberto](duvidas_em_aberto_evertecreg.md);
4. leve 3 perguntas da secao anterior para validar ao vivo.

Com esse roteiro, voce acompanha melhor o contexto e identifica rapido quando a conversa saiu de requisito e entrou em detalhe tecnico.