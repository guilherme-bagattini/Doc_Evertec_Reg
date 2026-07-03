# Resumo dos PDFs do EvertecReg

Os dois PDFs adicionados sao materiais de especificacao interna do projeto EvertecReg e funcionam como base de orientacao para produto, UX, frontend e regras de negocio.

## O que os documentos cobrem

- Cadastro e configuracao do cliente, com produtos, areas, colaboradores, documentacao, regras de negocio e integracoes.
- Configuracao de execucoes de crawling e scraping, incluindo horarios, fontes e reexecucoes.
- Reguladores, fontes e regras de descarte automatico.
- Tela de consulta de logs e historico tecnico das execucoes.
- Area de descarte, dashboard e visoes internas de operacao.
- Rastreabilidade, versionamento e logs de alteracoes em toda a plataforma.

## Pontos de negocio e produto mais fortes

- Alteracoes so devem ser persistidas com acao explicita de salvar.
- Mudancas em configuracoes futuras nao podem interferir em execucoes que ja estao em andamento.
- O sistema precisa preservar historico, auditoria e versionamento.
- A documentacao cadastrada serve como referencia para a IA e para os fluxos de analise.
- O contexto e fortemente multitenant, com escopo por company_id.

## Areas funcionais principais identificadas

- Configuracoes do cliente.
- Configuracoes de execucoes.
- Reguladores e fontes.
- Logs e historico de scraping.
- Dashboard e area de descarte.
- Regras de integracao, notificacao e auditoria.

## Leitura pratica para orientar o projeto

Se a ideia for organizar o trabalho daqui para frente, estes PDFs apontam que o produto depende de quatro eixos centrais:

1. configuracao do cliente e de suas estruturas internas;
2. automacao de coleta e controle de execucoes;
3. observabilidade e auditoria tecnica;
4. fluxo de analise/curadoria apoiado por IA.

## Observacao

Os PDFs estao em [orientacao_projeto](.) e devem ser usados como material de consulta, nao como base para alteracoes diretas do conteudo oficial.