# Base de conhecimento do CompliAsset para orientacao de demandas

## Finalidade

Este documento deve ser consultado como base de contexto funcional e de fontes sempre que uma nova demanda, melhoria, bug, duvida funcional ou necessidade de investigacao for transformada em card. Para o processo de trabalho de PM e PO, consulte o [Guia de definicao e abertura de cards: PM e PO](guia_abertura_cards_pm_po.md).

O objetivo e garantir que a demanda:

- esteja ligada ao funcionamento real do CompliAsset e do EvertecReg;
- descreva um problema ou resultado esperado, e nao apenas uma ideia solta;
- tenha contexto suficiente para produto, design, desenvolvimento e validacao;
- seja rastreavel ate a fonte da necessidade;
- possa ser priorizada e testada.

## Como usar este guia

Antes de abrir um card:

1. Consulte o artigo relacionado ao modulo ou fluxo.
2. Separe o que esta documentado do que ainda e hipotese ou decisao pendente.
3. Preencha o template e inclua somente as evidencias necessarias.
4. Copie para o card as regras aplicaveis, os criterios de aceite e as duvidas que dependem de validacao.

Este arquivo orienta a escrita e a analise da demanda. Ele nao substitui a validacao da versao atual do sistema, nem transforma automaticamente um artigo em requisito de implementacao.

## Relacao com o guia de PM e PO

Esta base e a fonte de contexto funcional, regras documentadas, artigos, referencias e pontos de validacao do CompliAsset. O [Guia de definicao e abertura de cards: PM e PO](guia_abertura_cards_pm_po.md) e a fonte do processo para transformar esse contexto em Product Brief, Planning, investigacao e cards executaveis.

Use os documentos nesta ordem quando uma nova demanda surgir:

1. No [guia de PM e PO](guia_abertura_cards_pm_po.md), capture a demanda e defina se ela precisa de Product Brief, discovery ou implementacao.
2. Nesta base, consulte o modulo, fluxo e artigos relacionados e registre as fontes e regras aplicaveis.
3. Volte ao [guia de PM e PO](guia_abertura_cards_pm_po.md) para organizar a matriz CSD, priorizar, escrever o card e definir a validacao.
4. No card, vincule esta base, as fontes consultadas e as decisoes ou duvidas que ainda dependem de confirmacao.

Quando houver conflito, a base preserva a fonte e o estado de confirmacao; ela nao autoriza implementar uma regra automaticamente. A decisao de produto deve ser registrada no card ou no documento de decisoes correspondente.

## Contexto permanente do produto

O CompliAsset e uma plataforma de GRC da Evertec. Ele apoia a execucao, o controle e a rastreabilidade de atividades de compliance, riscos e governanca.

A plataforma pode envolver:

- obrigacoes regulatorias, politicas, controles e evidencias;
- atividades, prazos, responsaveis e agenda regulatoria;
- ocorrencias, documentos, formularios, relacionados e checklists;
- background check, due diligence e sanctions screening;
- gestao de riscos e enquadramento;
- treinamentos, aceites, canal de denuncias e privacidade.

O EvertecReg e uma frente de inteligencia regulatoria dentro desse ecossistema. Seu papel e capturar e filtrar informacoes regulatorias, analisar impactos com apoio de IA e regras de negocio e distribuir acoes para execucao, inclusive por integracoes como Jira e Teams.

### Posicionamento institucional da CompliAsset

De acordo com o [site institucional da CompliAsset](https://www.compliasset.com/), a empresa apresenta a plataforma como um sistema de gestao de compliance e riscos, com foco em:

- centralizar obrigacoes, politicas, controles e evidencias;
- acompanhar atividades, prazos e responsabilidades;
- identificar, avaliar e monitorar riscos com controles e rastreabilidade;
- disponibilizar treinamentos de prateleira e customizados;
- operar canais de denuncias e de protecao de dados;
- apoiar PLD/FTP, KYC, KYP, due diligence e monitoramento de listas restritivas;
- disponibilizar conteudo regulatorio mapeado periodicamente e distribuicao de responsabilidades.

Use o site para entender o posicionamento, os modulos e a linguagem institucional do produto. Para definir comportamento de tela, permissao, validacao, integracao ou criterio de aceite, priorize artigos da Central de Ajuda, documentacao tecnica e validacoes com as areas responsaveis. Descricoes institucionais de capacidade nao devem ser interpretadas sozinhas como garantia de que uma funcao existe em todos os planos, ambientes ou configuracoes.

Ao analisar uma demanda, considere sempre tres perguntas:

1. O que precisa ser interpretado do ponto de vista regulatorio?
2. O que precisa virar tarefa, decisao ou acao operacional?
3. O que precisa ser registrado para gerar evidencia, historico e auditoria?

### Estruturacao do sistema

Com base no artigo [Entendendo a Estruturacao do Sistema](https://intercom.help/compliasset/pt-BR/articles/8330876-entendendo-a-estruturacao-do-sistema), publicado em 3 de junho de 2026, a estrutura funcional se organiza nos eixos abaixo.

#### Triangulo do Compliance

| Area | Definicao |
|---|---|
| Agenda | Atividades criadas pelo time juridico do CompliAsset ou pelo compliance da empresa, com prazo e recorrencia. |
| Obrigacoes | Registros criados pelo time juridico do CompliAsset ou pelo compliance da empresa, sem prazo nem recorrencia. |
| Eventos | Ocorrencias pontuais, previsiveis ou nao, que devem ser registradas pelo time de compliance ou pelos Colaboradores. |

Todas as tres areas possuem um dossie, entendido como o repositorio de informacoes relacionadas a Atividade, Obrigacao ou Evento. O dossie reune evidencias, colaboracao do time de compliance e atualizacao de status entre `Em Aberto`, `Em Andamento`, `Em Aprovacao`, `Concluido` e `Nao Realizado`.

#### Relacionados

Os Relacionados conectam cadastros a outros campos para apoiar organizacao e acompanhamento:

- `Colaboradores` podem ter acesso habilitado ao sistema e participar de treinamentos, formularios e outras demandas;
- `Fundos` e `Investidores` sao registros para cadastro e acompanhamento, sem acesso a plataforma;
- `Terceiros` tambem nao acessam a plataforma, mas seu perfil pode passar por Due Diligence;
- cada relacionado possui perfil individual para alimentar informacoes, extrair dossies reputacionais, anexar documentos ou evidencias e ser associado como Envolvido em Eventos.

#### Campanhas

O artigo entende Campanha como uma divulgacao a Colaboradores capaz de desencadear acoes, como geracao de relatorios, cobranca de preenchimento e inclusao de novos Colaboradores mesmo depois de iniciada. As areas apresentadas sao:

| Area | Finalidade |
|---|---|
| Aceites de Documentos | Circular documento que exige a manifestacao `Li, entendi e estou de acordo`. |
| Treinamentos | Capacitar Colaboradores em um tema e acompanhar sua evolucao. |
| Formularios | Solicitar dados especificos e personalizados para decisao ou analise interna. |
| Checklist | Dividir uma demanda em tarefas rastreaveis no dossie, com responsavel, prazo e evidencias. |

As regras especificas de destinatarios, versoes, prazos, status e permissoes de cada modulo devem ser consultadas nas respectivas secoes deste guia. A classificacao apresentada neste artigo nao permite presumir que todo comportamento de campanha se aplica a Checklist.

#### Como essa estrutura deve orientar um card

- Classificar primeiro a demanda como Agenda, Obrigacao, Evento, Relacionado, Campanha ou Checklist e registrar os vinculos entre essas entidades antes de definir uma solucao.
- Para Agenda e Obrigacoes, distinguir prazo e recorrencia; para Eventos, registrar se a ocorrencia e pontual, previsivel ou nao e quem a reportou.
- Preservar o dossie, suas evidencias, envolvidos, discussoes e historico de status; nao tratar uma mudanca de status como substituicao ou exclusao do fato registrado.
- Separar cadastro de Relacionado do acesso a plataforma: Fundos, Investidores e Terceiros nao devem receber acesso por serem cadastrados, e Colaboradores devem ter acesso habilitado conforme seu perfil e demanda.
- Para Campanhas, registrar publico, modulo, acao esperada, relatorios, cobrancas e impacto de inclusoes posteriores, aplicando as regras particulares de Aceites, Treinamentos e Formularios.
- Confirmar com produto a definicao atual de prazo e recorrencia, transicoes e permissao de status dos dossies, tipos de Relacionado elegiveis como Envolvidos, comportamento de inclusoes apos o inicio de cada Campanha e os limites entre Campanha e Checklist.

### Atribuicoes do perfil Colaborador

Com base no artigo [Atribuicoes do Perfil Colaborador](https://intercom.help/compliasset/pt-BR/articles/7183438-atribuicoes-do-perfil-colaborador), publicado em 20 de maio de 2026:

- o perfil Colaborador atua na colaboracao e no cumprimento de obrigacoes e atividades relacionadas ao time de Compliance;
- o `Painel de Controle` e a area inicial da visao de Colaborador e centraliza documentos pendentes de aceite, treinamentos, formularios, tarefas atribuidas, atividades em aberto e registros a reportar ao time de Compliance;
- cada cartao do Painel pode abrir uma visao ampliada por `Ver Todos` ou pelo menu lateral; o primeiro cartao exibe o responsavel pelo Canal de Compliance indicado pelos administradores;
- em `Aceites de Documentos`, os itens sao organizados nas abas `Pendente(s)`, `Aceito(s)`, `Recusado(s)` e `Todos`; depois da assinatura, o status passa automaticamente de `Em Aberto` para `Concluido`;
- `Reportes de Compliance` sao Eventos que podem ser criados pelo Colaborador ou disponibilizados por Membros para colaboracao; o artigo informa que podem ser iniciados pelos atalhos do Painel ou pela secao de Reportes;
- os Reportes formam dossies que podem ser acompanhados, comentados e usados como repositorio de evidencias;
- em `Tarefas`, o Colaborador consulta checklists atribuidas, abre o painel lateral com prazo, descricao e discussao e conclui a tarefa por `Concluir tarefa`;
- em `Treinamentos`, o Colaborador consulta itens pendentes e concluidos e pode baixar o certificado por `Baixar Certificado`; o certificado pode levar alguns minutos para ser processado e fica disponivel nas visoes de Colaborador e Membro;
- na `Agenda Regulatoria`, o Colaborador consulta as atividades sob sua responsabilidade, acompanha prazos, adiciona evidencias e utiliza `Discussao` para mencionar o time de Compliance;
- na `Biblioteca de Documentos`, consulta documentos compartilhados por Membros, como politicas, manuais e procedimentos internos;
- em `Formularios`, o Colaborador preenche solicitacoes pendentes ou formularios disponiveis para resposta a qualquer momento, mas nao cria novos formularios;
- para formularios preenchidos, o artigo descreve as acoes `Visualizar`, `Imprimir` e `Baixar Respostas`, com respostas em PDF, alem do acesso ao dossie e a discussao do time de Compliance;
- a `Central de Ajuda` e acessivel pelo ultimo icone do menu do Colaborador e oferece orientacoes para uso autonomo do sistema.

#### Como essa regra deve orientar um card

- Registrar perfil, visao utilizada, ambiente, cartao ou secao, dossie relacionado, acao executada, status, prazo, evidencia e resultado esperado.
- Validar o isolamento da visao de Colaborador: o perfil deve acessar somente demandas, documentos, treinamentos, formularios, tarefas e atividades efetivamente concedidos.
- Para o Painel, conferir os cartoes, o responsavel exibido pelo Canal de Compliance, a correspondencia com os dossies de origem, `Ver Todos` e a navegacao pelo menu lateral, sem ampliar permissoes.
- Para Aceites, testar abas, transicao de status, abertura do documento, aceite, recusa, justificativa e preservacao do historico conforme as regras especificas do modulo.
- Para Reportes e Tarefas, validar criacao ou recebimento do Evento, discussao, evidencias, atribuicao, prazo, conclusao e acesso ao dossie, sem confundir Evento, checklist e plano de acao.
- Para Treinamentos, testar progresso, conclusao, processamento assincrono e disponibilidade do certificado nas visoes de Colaborador e Membro.
- Para Agenda e Biblioteca, validar que o Colaborador pode adicionar evidencias e consultar somente documentos compartilhados, respeitando permissoes, visibilidade, versoes e retencao.
- Para Formularios, bloquear a criacao pelo Colaborador, preservar respostas enviadas, validar `Visualizar`, `Imprimir`, `Baixar Respostas` e o acesso a discussao, sem permitir edicao retroativa sem regra formal.
- Confirmar com produto a lista vigente de cartoes e secoes, a diferenca entre Reportes, Eventos, Tarefas e Planos de Acao, o alcance de `Ver Todos`, as permissoes de comentario e evidencia, a disponibilidade de formularios isolados e a auditoria das acoes do Colaborador.

### Alteracao de Colaborador para Membro

Com base no artigo [Alteracao de Colaborador para Membro](https://intercom.help/compliasset/pt-BR/articles/7153535-alteracao-de-colaborador-para-membro), publicado em 24 de outubro de 2024:

- o sistema possui quatro perfis de acesso: Super Administrador, Membro-Administrador, Membro-Usuario e Colaborador;
- o perfil Colaborador e destinado a pessoas que nao integram o time de Compliance e utiliza a `Visao do Colaborador`, com acesso limitado a treinamentos, aceites de documentos, formularios e demandas atribuidas;
- quando o Colaborador precisa assumir responsabilidades adicionais, como gerenciar uma secao do sistema, ele pode ser promovido para um perfil de Membro;
- a promocao ocorre em `Configuracoes` > `Membros`, pela acao `+`, com preenchimento das informacoes solicitadas e selecao das areas de acesso;
- as areas podem ser escolhidas conforme a funcao, incluindo exemplos como `Agenda`, `Eventos`, `Investidores` e `Terceiros`, sem necessidade de liberar todas as funcionalidades;
- para um Colaborador que auxilia uma funcao especifica, o artigo recomenda o perfil `Membro-Usuario`, com acesso limitado as ferramentas necessarias;
- somente Membros com permissoes de Administrador podem criar e ajustar perfis de Membros-Usuarios;
- quando um novo Colaborador ingressa no time de Compliance, o administrador deve cadastra-lo primeiro como `Novo Colaborador` e depois criar e configurar seu perfil de Membro.

#### Como essa regra deve orientar um card

- Tratar a promocao como mudanca de identidade de acesso e registrar Colaborador de origem, perfil novo, areas liberadas, responsavel, motivo, ambiente e resultado efetivo.
- Validar a pre-condicao de cadastro como Colaborador antes da criacao do Membro e testar as transicoes entre Colaborador, Membro-Usuario e Membro-Administrador conforme a permissao vigente.
- Aplicar menor privilegio: liberar somente as secoes necessarias para a funcao e verificar que a visibilidade de uma secao nao concede acoes além da matriz de permissoes aplicavel.
- Restringir criacao e ajuste de Membros-Usuarios a Membros-Administradores, incluindo tentativas por menu, URL direta, API e sessao ativa.
- Testar acesso efetivo antes e depois da promocao, incluindo revogacao ou reducao de secoes, sessoes ativas, notificacoes, responsabilidades, auditoria e preservacao do historico do Colaborador.
- Diferenciar promocao para Membro de simples atribuicao de uma demanda na Visao do Colaborador; a mudanca de perfil nao deve ser usada para contornar regras de atribuicao ou ampliar acesso sem justificativa.
- Confirmar com produto e seguranca a lista de areas configuraveis, a diferenca entre Membro-Usuario e Membro-Administrador, os efeitos em sessoes e tarefas existentes, a protecao do Super Administrador e a retencao do historico de acesso.

### Compartilhamento de Fundos, Investidores e Terceiros com Colaboradores

Com base no artigo [Compartilhar Fundos, Investidores e Terceiros com Colaboradores](https://intercom.help/compliasset/pt-BR/articles/5596387-compartilhar-fundos-investidores-e-terceiros-com-colaboradores), publicado em 20 de setembro de 2024:

- a funcionalidade permite envolver um Colaborador em um perfil especifico de Fundo, Investidor ou Terceiro sem transforma-lo em Membro do sistema;
- o compartilhamento e iniciado no perfil do Relacionado, na area `Discussao` > `Permissao de Acessos` > `Convidar Colaborador`;
- o convite pode enviar ou nao uma notificacao por e-mail ao Colaborador;
- quando a notificacao for enviada, o usuario define o assunto e a mensagem do e-mail;
- a permissao pode ficar ativa por 30, 180 ou 365 dias, ou por tempo indeterminado;
- a confirmacao ocorre pela acao `Convidar Colaborador`;
- depois do compartilhamento, o perfil aparece na secao correspondente da `Visao do Colaborador`, como `Fundos`, `Investidores` ou `Terceiros`;
- dentro do perfil compartilhado, o Colaborador pode enviar comentarios e anexar arquivos, mas nao pode editar ou excluir as demais informacoes do cadastro.

#### Como essa regra deve orientar um card

- Registrar Relacionado de origem, tipo de cadastro, Colaborador convidado, usuario que concedeu o acesso, data, prazo, notificacao, assunto e resultado, minimizando dados pessoais nas evidencias.
- Validar o caminho `Discussao` > `Permissao de Acessos` > `Convidar Colaborador`, a selecao do prazo e a confirmacao do convite.
- Testar os prazos de 30, 180 e 365 dias e a opcao indeterminada, incluindo expiracao, revogacao, renovacao e comportamento apos o prazo.
- Testar notificacao habilitada e desabilitada, conferindo assunto, mensagem, destinatario e ausencia de envio quando a opcao estiver desmarcada.
- Validar que o perfil aparece somente para o Colaborador autorizado, na secao correta, e que o acesso nao concede visibilidade a outros Relacionados ou areas do sistema.
- Garantir que o Colaborador pode comentar e anexar arquivos, mas nao editar, excluir ou alterar os dados cadastrais do Fundo, Investidor ou Terceiro.
- Diferenciar compartilhamento de perfil especifico de promocao para Membro e de atribuicao de uma demanda; nenhum desses fluxos deve conceder acesso amplo por inferencia.
- Confirmar com produto e seguranca quem pode convidar, revogar ou renovar a permissao, os efeitos em sessoes ativas, notificacoes, anexos, auditoria, retencao e isolamento entre empresas e ambientes.

### Cadastro de Investidores

Com base no artigo [Cadastro de Investidores](https://intercom.help/compliasset/pt-BR/articles/4360283-cadastro-de-investidores), publicado em 30 de setembro de 2025:

- o cadastro pode ser iniciado em `Investidores` > `Novo Investidor` ou em `Todos os Investidores` > `+`;
- o perfil deve ser classificado como Pessoa Juridica, Pessoa Fisica ou Estrangeiro;
- conforme o tipo, o cadastro utiliza CNPJ, CPF ou Documento, alem de Razao Social ou Nome Completo, Nome fantasia quando aplicavel, E-mail e Risco;
- todos os tipos podem receber `Data de entrada`, `Data de saida` e vinculacao a um Grupo;
- a inclusao e concluida pela acao `Confirmar`;
- em `Todos os Investidores`, e possivel acessar, editar, excluir e exportar cadastros;
- o perfil apresenta informacoes gerais, `Eventos Relacionados`, `Dossie Reputacional do Data Engine` e `Discussao` para comentarios, anotacoes e anexos;
- uma Data de saida passada transfere automaticamente o Investidor de `Ativos` para `Inativos`.

#### Como essa regra deve orientar um card

- Registrar tipo de pessoa, identificador, nome ou razao social, e-mail, risco, datas, Grupo, usuario executor, ambiente, acao e resultado, minimizando documentos pessoais nas evidencias.
- Validar os caminhos de cadastro manual e por lote, os campos dependentes do tipo de pessoa, `Confirmar`, persistencia, edicao, exclusao e exportacao.
- Testar Data de entrada, Data de saida passada ou futura, transicao entre `Ativos` e `Inativos`, reabertura do perfil e efeitos sobre Eventos e Grupos.
- Conferir que `Eventos Relacionados`, Dossie Reputacional e `Discussao` respeitam as permissoes do perfil, preservam historico e nao ampliam acesso por estarem disponiveis no cadastro.
- Diferenciar cadastro, exportacao, Dossie Reputacional e envolvimento em Evento; confirmar formatos, custos, limites, auditoria, retencao e comportamento de exclusao.
- Confirmar com produto, seguranca e privacidade campos obrigatorios por tipo de pessoa, validacao de CPF/CNPJ/Documento, regras de risco, filtros de Ativos e Inativos, permissao de exportacao e efeitos em Grupos e Eventos existentes.

### Categorizar Colaboradores em Funcoes

Com base no artigo [Categorizar Colaboradores em Funcoes](https://intercom.help/compliasset/pt-BR/articles/4636444-categorizar-colaboradores-em-funcoes), publicado em 23 de maio de 2025:

- `Funcoes` classificam e agrupam perfis de Colaboradores conforme suas atribuicoes e vinculos com a empresa;
- exemplos de categorias incluem socios, terceirizados, funcionarios, profissionais part-time, profissionais full-time e consultores externos;
- o acesso ocorre em `Configuracoes` > `Funcoes`;
- a acao `+` cria uma nova funcao;
- depois de criada, a funcao permite usar `Adicionar colaborador` para associar Colaboradores e consultar todos os vinculados;
- uma funcao existente pode ter o titulo editado ou ser excluida;
- durante a criacao ou edicao do perfil de um Colaborador, a secao `Funcao(oes)` permite criar novas funcoes e vincular as funcoes disponiveis;
- a associacao feita no perfil e salva pela acao `Confirmar`.

#### Como essa regra deve orientar um card

- Registrar funcao, Colaborador, acao de criacao, edicao, exclusao ou associacao, usuario executor, empresa ou ambiente e resultado da operacao.
- Validar o caminho `Configuracoes` > `Funcoes`, a criacao por `+`, a inclusao por `Adicionar colaborador`, a consulta de vinculados, a edicao do titulo e a exclusao da funcao.
- Testar a criacao e vinculacao de funcoes tanto na tela de Funcoes quanto no perfil de um Colaborador, confirmando a persistencia por `Confirmar`.
- Diferenciar Funcao de Grupo e Departamento: Funcao categoriza Colaboradores, Grupo apoia selecoes e associacoes em outros fluxos e Departamento funciona como atributo e filtro cadastral.
- Validar associacoes multiplas quando permitidas, remocao de uma funcao do perfil, duplicidade, consistencia da listagem e efeitos sobre filtros e campanhas que utilizem a classificacao.
- Nao presumir que excluir uma funcao remove ou altera Colaboradores vinculados; confirmar o comportamento, o historico, a auditoria e o tratamento de funcoes usadas em filtros ou registros existentes.
- Confirmar com produto as permissoes para criar, editar, associar e excluir funcoes, as regras de nomes e duplicidade, o limite de associacoes, a visibilidade por perfil e o impacto em Eventos, campanhas, filtros e relatorios.

### Mandatos de Colaboradores

Com base no artigo [Mandatos de Colaboradores](https://intercom.help/compliasset/pt-BR/articles/9516488-mandatos-de-colaboradores), publicado em 22 de agosto de 2024:

- Mandato registra a autorizacao formal de um Colaborador para tomar decisoes ou realizar transacoes financeiras em nome da empresa, com poderes e limites de atuacao;
- o Colaborador precisa estar cadastrado antes que um Mandato seja adicionado;
- o acesso ocorre em `Colaboradores` > `Todos os Colaboradores`, abrindo o perfil pelo nome;
- no perfil, a area `Mandatos` fica proxima de `Resumo Profissional`;
- `Adicionar` permite cadastrar `Posicao`, `Descricao`, `Data de inicio` e `Data de termino`, quando houver;
- depois da inclusao, as acoes `Editar` e `Excluir` ficam disponiveis junto ao registro;
- inclusoes, edicoes e exclusoes de Mandatos ficam registradas em `Historico`, dentro de `Discussao` no perfil do Colaborador.

#### Como essa regra deve orientar um card

- Registrar Colaborador, Mandato, posicao, descricao, datas, usuario executor, acao realizada, resultado e evento correspondente no Historico.
- Validar a pre-condicao de cadastro do Colaborador e o caminho `Mandatos` > `Adicionar`, incluindo data de termino ausente ou preenchida.
- Testar edicao e exclusao do Mandato, preservando o cadastro do Colaborador e registrando cada alteracao no Historico da Discussao.
- Tratar poderes, limites, inicio e termino como dados sensiveis de governanca e autoridade; aplicar permissao, auditoria, retencao e minimizacao nas evidencias.
- Confirmar com produto e seguranca os perfis autorizados, campos obrigatorios, formato e validacao de datas, possibilidade de multiplos Mandatos, sobreposicao de vigencias, impacto em tarefas ou Eventos e comportamento apos a exclusao.

### Certificacoes de Colaboradores

Com base no artigo [Certificacoes de Colaboradores](https://intercom.help/compliasset/pt-BR/articles/9761125-certificacoes-de-colaboradores), publicado em 16 de junho de 2026:

- certificacoes registram conhecimentos e habilidades profissionais relevantes para a atuacao no mercado financeiro e para a conformidade regulatoria;
- o Colaborador precisa estar cadastrado antes que uma certificacao seja adicionada;
- o acesso ocorre em `Colaboradores` > `Todos os Colaboradores`, abrindo o perfil pelo nome;
- no perfil, a area `Certificacoes` fica no inicio da tela, ao lado de `Mandatos`;
- `Adicionar` permite cadastrar `Nome`, `Data de inicio`, `Data de vencimento/validade`, `Numero de registro` e um arquivo ou certificado opcional;
- a certificacao pode ser editada ou excluida, e o anexo pode ser baixado;
- `Adicionar periodo` permite registrar `Data de inicio PEC`, `Data final`, a pontuacao numerica a ser realizada no periodo e `Observacoes` opcionais;
- em `Acoes`, e possivel editar ou remover um periodo, incluir nova pontuacao ou excluir pontuacao cadastrada;
- inclusoes e exclusoes de certificacoes ficam registradas em `Historico`, dentro de `Discussao` no perfil do Colaborador;
- notificacoes de vencimento sao enviadas por e-mail aos usuarios configurados como `Assinantes` no perfil e ao proprio Colaborador, com alertas 90, 60 e 30 dias antes do vencimento.

#### Como essa regra deve orientar um card

- Registrar Colaborador, certificacao, nome, datas, numero de registro, anexo, periodo PEC, pontuacao, observacoes, assinantes, usuario executor, acao, notificacao e resultado.
- Validar a pre-condicao de cadastro do Colaborador e o caminho `Certificacoes` > `Adicionar`, incluindo anexo opcional e data de vencimento/validade.
- Testar inclusao, edicao, exclusao e download do anexo sem confundir a exclusao da certificacao com a exclusao de um periodo ou pontuacao.
- Validar `Adicionar periodo`, `Acoes`, datas da PEC, pontuacao numerica, observacoes opcionais e a possibilidade de multiplos periodos ou pontuacoes conforme a regra vigente.
- Conferir que alteracoes e exclusoes relevantes ficam no `Historico` da `Discussao`, preservando o registro original e a trilha de auditoria.
- Testar alertas por e-mail em 90, 60 e 30 dias, destinatarios `Assinantes` e Colaborador, duplicidade, vencimento sem renovacao e comportamento quando a data e alterada ou a certificacao e excluida.
- Tratar certificacao, numero de registro, anexo e pontuacao como dados de qualificacao profissional; aplicar permissoes, retencao, minimizacao e controles de acesso nas evidencias.
- Confirmar com produto, seguranca e Compliance os perfis autorizados, campos obrigatorios, formatos e limites de anexo, unidade e regra da pontuacao, sobreposicao de periodos, calculo de vencimento, calendario dos alertas, auditoria e tratamento de certificacoes expiradas.

### Investimentos Pessoais de Colaboradores

Com base no artigo [Investimentos Pessoais de Colaboradores](https://intercom.help/compliasset/pt-BR/articles/4951125-investimentos-pessoais-de-colaboradores), publicado em 24 de outubro de 2024:

- os destinatarios das solicitacoes de investimentos pessoais sao definidos em `Configuracoes` > `Canal de Compliance`, no campo `Destinatario(s)`;
- os destinatarios selecionados recebem notificacao por e-mail sempre que uma solicitacao e realizada;
- a publicacao dos destinatarios ocorre pela acao `Definir e Publicar`;
- o e-mail de notificacao permite abrir o pedido por `Ver Evento`;
- reportes criados pelo Canal de Compliance geram novos Eventos, diferenciados pela natureza utilizada;
- os pedidos sao localizados em `Todos os Eventos` usando o filtro de natureza `Investimentos Pessoais de Colaboradores`;
- no dossie, o pedido inicia com status `Pendente de aprovacao`;
- depois da analise do time de Compliance, o status pode ser alterado para `Deferido` ou `Indeferido`;
- durante a analise, e possivel definir responsavel, alterar o risco e inserir comentarios no dossie;
- depois da alteracao do pedido, o status geral do Evento passa para `Concluido` e o Colaborador recebe a resposta por e-mail.

#### Como essa regra deve orientar um card

- Registrar canal, empresa ou ambiente, destinatarios anteriores e novos, publicacao, colaborador solicitante, Evento, natureza, status, responsavel, risco, comentarios, decisao e notificacoes.
- Validar a configuracao em `Configuracoes` > `Canal de Compliance`, a selecao de um ou mais destinatarios e o efeito somente apos `Definir e Publicar`.
- Testar notificacao por e-mail, `Ver Evento`, localizacao em `Todos os Eventos` e filtro pela natureza correta, sem expor pedidos de outros ambientes ou colaboradores.
- Validar o ciclo pendente de aprovacao, `Deferido`, `Indeferido` e `Concluido`, preservando o historico da decisao e a correspondencia entre o Evento e a resposta enviada.
- Testar definicao de responsavel, alteracao de risco e comentarios sem permitir que uma acao substitua ou apague o pedido original do Colaborador.
- Confirmar com produto, seguranca e privacidade os perfis autorizados, destinatarios, conteudo e prazo das notificacoes, permissao de acesso ao dossie, auditoria, retencao e tratamento de dados pessoais e informacoes potencialmente sensiveis do investimento.

### Editar Atalhos na Visao de Colaborador

Com base no artigo [Editar 'Atalhos' na Visao de Colaborador](https://intercom.help/compliasset/pt-BR/articles/4561615-editar-atalhos-na-visao-de-colaborador), publicado em 5 de dezembro de 2024:

- a configuracao ocorre em `Configuracoes` > `Natureza de Eventos`;
- essa secao fica disponivel somente para usuarios com acesso de Membro-Administrador;
- a listagem de naturezas possui a coluna `Novos Eventos`, que define as naturezas disponiveis para Membros, usuarios e administradores, ao criar novos Eventos;
- a coluna `Canal de Compliance` define as naturezas disponiveis na `Visao do Colaborador`, para criacao de Reportes de Compliance;
- uma natureza nao pode ser disponibilizada apenas em `Canal de Compliance`; primeiro deve estar habilitada em `Novos Eventos`;
- a persistencia das selecoes ocorre pela acao `Confirmar`;
- depois da habilitacao, a natureza aparece em `Atalhos` no `Painel de Controle` da Visao do Colaborador;
- ao selecionar `Criar`, o Colaborador descreve o reporte e gera um novo Evento para tratamento pelo time de Compliance.

#### Como essa regra deve orientar um card

- Registrar natureza, ambiente, Membro-Administrador executor, estado anterior e novo nas colunas `Novos Eventos` e `Canal de Compliance`, data de confirmacao e resultado na Visao do Colaborador.
- Validar o bloqueio de `Configuracoes` > `Natureza de Eventos` para perfis sem acesso de Membro-Administrador, inclusive por URL direta, API e sessao ativa.
- Testar habilitacao em `Novos Eventos`, habilitacao conjunta no `Canal de Compliance`, desabilitacao e tentativa de habilitar somente a segunda coluna.
- Conferir que apenas `Confirmar` persiste a selecao e que as naturezas habilitadas aparecem em `Atalhos` sem disponibilizar outras naturezas ou secoes do sistema.
- Validar a criacao do Reporte por `Atalhos` > `Criar`, a natureza do Evento gerado, o dossie de destino, os destinatarios e a aplicacao das permissoes do Colaborador.
- Confirmar com produto a lista editavel de naturezas, a semantica das duas colunas, o comportamento ao desabilitar uma natureza ja usada, a auditoria, as notificacoes, os efeitos em Eventos existentes e as permissoes de criar e tratar os reportes.

### Desativar Acesso de Colaborador

Com base no artigo [Desativar Acesso de Colaborador](https://intercom.help/compliasset/pt-BR/articles/4582671-desativar-acesso-de-colaborador), publicado em 22 de novembro de 2024:

- o desligamento e iniciado em `Colaboradores` > `Todos os Colaboradores`, na listagem `Time Atual`, pela acao `Editar` do Colaborador;
- a desativacao ocorre ao preencher `Data de Demissao` e selecionar `Confirmar`;
- depois da confirmacao, o Colaborador sai de `Time Atual` e passa para `Ex-Colaboradores`, perdendo o acesso ao sistema;
- comentarios, arquivos e historico de atividades permanecem salvos apos a desativacao;
- a secao `Futuro Responsavel` permite selecionar outro Colaborador para assumir responsabilidades do desligado;
- o novo responsavel assume tarefas relacionadas a Atividades, Obrigacoes e Eventos do Colaborador desligado;
- a transferencia se aplica somente a itens com status `Em Aberto`;
- para uma Data de Demissao futura, a transferencia ocorre automaticamente ao final do dia do desligamento;
- para desligamentos com data retroativa ou no mesmo dia, a transferencia ocorre imediatamente;
- a selecao do Futuro Responsavel tambem deve ser salva pela acao `Confirmar`;
- a desativacao de acesso e diferente da exclusao do perfil, que segue um fluxo separado.

#### Como essa regra deve orientar um card

- Registrar Colaborador desligado, Data de Demissao, Membro executor, Futuro Responsavel, data e hora da confirmacao, estado das listagens e resultado da transferencia.
- Validar bloqueio de acesso, sessao ativa, notificacoes, downloads, integracoes e acesso a dossies apos a passagem para `Ex-Colaboradores`, preservando comentarios, arquivos, responsabilidades e historico.
- Testar datas futuras, retroativas e do mesmo dia, conferindo o momento efetivo da transferencia e o tratamento de fuso horario ou fim do dia.
- Validar que somente Atividades, Obrigacoes e Eventos `Em Aberto` sao transferidos e que itens concluidos, encerrados ou em outros status preservam o responsavel e o historico original.
- Testar o fluxo sem Futuro Responsavel, com substituto selecionado, com responsabilidades conflitantes e com mais de um tipo de dossie, sem apagar a atribuicao anterior.
- Diferenciar desativacao, transferencia de responsabilidades, retorno de acesso e exclusao de Colaborador; nao usar a exclusao para simular desligamento.
- Confirmar com produto e seguranca os perfis autorizados, o momento de bloqueio, o comportamento de sessoes existentes, regras de recontratacao, notificacoes, auditoria, retencao e tratamento de tarefas sem substituto.

### Retornar Acesso de Ex-Colaborador

Com base no artigo [Retornar Acesso de Ex-Colaborador](https://intercom.help/compliasset/pt-BR/articles/8733090-retornar-acesso-de-ex-colaborador), publicado em 19 de agosto de 2024:

- Ex-Colaboradores ficam listados em `Colaboradores` > `Todos os Colaboradores` > `Ex-Colaboradores` quando o acesso foi desativado por Data de Demissao;
- Colaboradores excluidos do sistema nao aparecem em `Ex-Colaboradores`, pois o cadastro foi removido;
- para reativar pelo perfil, o usuario seleciona `Editar`, apaga o valor de `Data de Demissao`, clica fora do campo para deixa-lo vazio e seleciona `Confirmar`;
- depois da confirmacao, o perfil retorna para `Time Atual` e o acesso e restabelecido com o mesmo login;
- quando varios Colaboradores precisam ser reativados, a acao pode ser feita por atualizacao em massa usando a mesma planilha de importacao de Colaboradores;
- na planilha, deve-se remover a Data de Demissao dos Colaboradores selecionados e importar o arquivo atualizado conforme as regras do upload;
- na atualizacao por planilha, o e-mail deve ser o mesmo do cadastro existente para que a reativacao seja concluida;
- se o modelo original nao estiver disponivel, deve ser baixado novamente e preenchido com os dados existentes no cadastro, mantendo a Data de Demissao em branco.

#### Como essa regra deve orientar um card

- Diferenciar retorno de acesso por remocao da Data de Demissao, reativacao em massa por planilha e recriacao de cadastro excluido; nao tratar esses fluxos como equivalentes.
- Validar listagem `Ex-Colaboradores`, busca, `Editar`, limpeza do campo, clique fora do campo, `Confirmar`, retorno para `Time Atual` e login preservado.
- Testar que cadastros excluidos nao podem ser reativados por essa listagem e exigem fluxo separado, preservando a distincao entre desativacao e exclusao.
- Para upload em massa, validar modelo, identificacao pelo mesmo e-mail, Data de Demissao vazia, pre-validacao, resultado por linha, limites, erros e processamento parcial ou rollback.
- Conferir a restauracao de acesso, sessoes, notificacoes, responsabilidades, dossies, integracoes e historico, sem apagar a evidencia do desligamento anterior.
- Confirmar com produto e seguranca quem pode reativar, o momento efetivo do desbloqueio, regras de recontratacao, expiracao de credenciais, auditoria e tratamento de e-mail divergente ou cadastro excluido.

### Exclusao de Colaboradores

Com base no artigo [Exclusao de Colaboradores](https://intercom.help/compliasset/pt-BR/articles/9970843-exclusao-de-colaboradores), publicado em 22 de novembro de 2024:

- para habilitar a exclusao, primeiro e necessario remover todas as atribuicoes, responsabilidades e permissoes associadas ao Colaborador;
- a verificacao deve abranger as listagens `Eventos de sua Responsabilidade`, `Eventos Relacionados`, `Eventos de Aceites`, `Eventos de Treinamento` e `Permissoes de Acesso`;
- tambem e necessario verificar a `Agenda` e as `Obrigacoes Estruturais` para identificar Atividades sob responsabilidade do Colaborador;
- depois da remocao de todos os vinculos em dossies, como envolvido, responsavel e usuario com permissao, a exclusao pode ser iniciada pela acao `Excluir` na listagem ou pelo icone de lixeira no perfil;
- a exclusao nao apaga comentarios feitos pelo Colaborador em dossies de Atividades e Obrigacoes Estruturais;
- quando um dossie de Evento associado ao Colaborador e removido, discussoes, assinaturas de documentos e demais informacoes daquele Evento podem ser permanentemente perdidas;
- para cadastrar novamente um Colaborador excluido, informar o e-mail na area de novos Colaboradores faz o sistema reconhecer e preencher Nome e E-mail anteriores;
- o novo cadastro nao restaura permissoes removidas nem responsabilidades anteriores;
- a exclusao deve ser tratada como operacao de alto impacto; o artigo recomenda desativar o perfil quando for necessario preservar dados e permitir consultas futuras.

#### Como essa regra deve orientar um card

- Registrar Colaborador, usuario executor, empresa ou ambiente, vinculos encontrados, responsabilidades, permissoes, dossies afetados, confirmacao da remocao e resultado da exclusao.
- Validar cada listagem de vinculos e tambem Agenda e Obrigacoes Estruturais antes de liberar `Excluir`; nao considerar apenas a ausencia de uma responsabilidade na tela principal.
- Testar exclusao pela listagem e pelo perfil, garantindo que a acao bloqueia enquanto houver envolvimento, responsabilidade ou permissao pendente.
- Diferenciar a preservacao de comentarios em Atividades e Obrigacoes da perda de dados de Eventos removidos, incluindo discussoes, assinaturas e evidencias associadas.
- Testar a recriacao por e-mail e confirmar que somente Nome e E-mail sao reaproveitados, sem restaurar acessos, responsabilidades, dossies ou permissoes anteriores.
- Preferir desativacao quando o objetivo for bloquear acesso sem eliminar o cadastro e os dados; nao usar exclusao para simular desligamento ou afastamento temporario.
- Tratar a exclusao de dossies e assinaturas como risco de retencao, auditoria e conformidade; exigir evidencia da decisao, permissao adequada, avaliacao de impacto e minimizacao de dados no card.
- Confirmar com produto, seguranca e Compliance as regras de exclusao em cascata, perfis autorizados, comportamento de sessoes, historico, notificacoes, integracoes, retencao, recuperacao e tratamento de Eventos, Aceites, Treinamentos e Formularios vinculados.

### Funcionalidades coringas na secao de Relacionados

Com base no artigo [7 Funcionalidades Coringas na Secao de Relacionados](https://intercom.help/compliasset/pt-BR/articles/15350862-7-funcionalidades-coringas-na-secao-de-relacionados), publicado em 3 de junho de 2026:

- a secao de Relacionados contempla `Colaboradores`, `Fundos`, `Investidores` e `Terceiros` e oferece atalhos para operacoes de compliance dentro dos perfis;
- no perfil de cada Colaborador, o botao `Reenviar` dispara um e-mail de boas-vindas com senha temporaria para tratar perda, expiracao ou ausencia da credencial inicial;
- nos perfis de Fundos, Investidores e Terceiros, o campo `Permissao de Acesso` permite vincular um Colaborador ao cadastro especifico, concedendo visibilidade por periodo definido ou por prazo indeterminado;
- no perfil de Colaboradores, `Mandatos` registra cargo, poderes de atuacao e periodo de vigencia;
- no perfil de Colaboradores, `Certificacoes` registra credenciais profissionais, datas, numero de registro, anexo e periodos de pontuacao `PEC` vinculados a cada certificacao;
- o campo `Dossie Reputacional`, integrado ao Data Engine, pode ser acessado em dossies de Atividades da Agenda, Obrigacoes Estruturais, Eventos e perfis de Colaboradores, Fundos, Investidores e Terceiros;
- o atalho `Criar Evento`, disponivel nos perfis de Relacionados, inicia um Evento com o perfil de origem preenchido automaticamente como Envolvido;
- o campo `Superior Imediato` do Colaborador registra a hierarquia e, quando o acesso do Colaborador e desativado, o superior cadastrado assume automaticamente as demandas que estavam sob sua responsabilidade;
- o perfil de Terceiro apresenta o painel de `Due Diligence`, no qual se configura o questionario, prazo de resposta e lembretes automaticos; o Terceiro recebe um e-mail com link para preenchimento e a documentacao retornada fica disponivel para avaliacao;
- depois da contratacao do Terceiro, a situacao pode ser alterada para `Contratado` e uma periodicidade de revisao pode ser definida para automatizar novos ciclos de DDQ.

#### Como essa regra deve orientar um card

- Classificar o cadastro de origem como Colaborador, Fundo, Investidor ou Terceiro e registrar o atalho, o usuario executor, a empresa ou ambiente e o resultado da operacao.
- Para `Permissao de Acesso`, validar que o Colaborador visualiza somente o cadastro especifico autorizado, respeitando periodo, prazo indeterminado, revogacao e permissoes do seu perfil; nao confundir essa vinculacao com acesso amplo a uma secao.
- Para `Reenviar`, preservar a obrigatoriedade de troca da senha temporaria e nao registrar credenciais, links ou tokens nas evidencias.
- Para Mandatos e Certificacoes, validar vigencia, datas, numero de registro, anexos, pontuacao `PEC`, historico e efeitos de expiracao ou alteracao, sem tratar esses campos como equivalentes a permissao de acesso.
- Para o Dossie Reputacional, validar origem, destinatario, custo quando aplicavel, resultado, acesso ao arquivo e protecao de dados pessoais, sem presumir que a disponibilidade do campo autoriza qualquer perfil a consultar o dossie.
- Para `Criar Evento`, validar que o Relacionado correto e associado automaticamente como Envolvido e que a criacao preserva as permissoes, historico e demais dados do perfil de origem.
- Para `Superior Imediato`, testar desativacao de Colaborador com e sem superior cadastrado, transferencia de demandas, conflitos de responsabilidade, notificacoes, historico e reversao, sem apagar a atribuicao original.
- Para Due Diligence de Terceiros, validar questionario, prazo, lembretes, envio do link, recebimento de documentos, avaliacao, mudanca para `Contratado`, periodicidade e novos ciclos de DDQ.
- Confirmar com produto e seguranca quem pode executar cada atalho, o alcance da visibilidade concedida, o momento da transferencia de demandas, o tratamento de sessoes e notificacoes, a retencao de documentos e dossies reputacionais e as regras de auditoria.

### Realizando DD Inicial e Periodica de Terceiros

Com base no artigo [Realizando DD Inicial e Periodica de Terceiros](https://intercom.help/compliasset/pt-BR/articles/7170567-realizando-dd-inicial-e-periodica-de-terceiros), publicado em 29 de abril de 2026:

- o processo de Due Diligence de Terceiros usa abordagem baseada em risco, recebe documentos enviados pelo Terceiro e pode gerar dossies reputacionais;
- o fluxo comeca pelo cadastro de um novo Terceiro ou pela abertura de um cadastro existente em `Todos os Terceiros`;
- no perfil do Terceiro, o painel `Due Diligence` inicia com a situacao `Selecao e Contratacao`;
- as situacoes disponiveis sao `Selecao e Contratacao`, `Contratado`, `Rescindido` e `Rejeitado`;
- na situacao inicial, e possivel selecionar uma ferramenta de `Background Check`, usando o Data Engine ou `Nenhuma`;
- o questionario pode ser um dos sete DDQs disponibilizados a partir da Anbima ou um questionario proprio armazenado na Biblioteca de Documentos;
- para usar questionario proprio, a opcao correspondente deve ser habilitada antes da selecao;
- o cadastro da DDQ exige prazo de resposta em dias corridos e pode habilitar e-mails de cobranca apos o vencimento;
- `Criar Due Diligence Inicial` abre automaticamente um Evento de Due Diligence Inicial vinculado ao Terceiro e envia e-mail ao endereco cadastrado com o link do questionario;
- o Terceiro envia o questionario respondido e os arquivos pelo link recebido; os documentos ficam no dossie do Evento, em `Discussao` > `Comentarios`;
- o Evento pode ser localizado em `Todos os Eventos` ou na aba `Eventos Relacionados` do perfil do Terceiro;
- `Solicitar Mais Informacoes do Terceiro` permite pedir novos dados ou arquivos quando a resposta estiver incompleta;
- quando selecionado, o Background Check integrado fica disponivel no perfil do Terceiro;
- ao mudar a situacao para `Contratado`, a empresa pode definir pontuacao, risco, data inicial da revisao e periodicidade da DDQ;
- `Iniciar Revisao Periodica` automatiza novos ciclos de Due Diligence conforme a periodicidade definida;
- contratos rescindidos ou recusados devem refletir a situacao correspondente no painel e podem exigir edicao posterior.

#### Como essa regra deve orientar um card

- Registrar Terceiro, situacao, questionario, versao, ferramenta de Background Check, prazo, cobrancas, Evento, documentos, solicitacoes adicionais, pontuacao, risco, revisao e resultado.
- Validar o cadastro ou selecao do Terceiro, o painel `Due Diligence`, as quatro situacoes e as transicoes permitidas, sem confundir `Rejeitado` com `Rescindido`.
- Testar questionario Anbima, questionario proprio da Biblioteca, habilitacao da opcao correspondente, prazo em dias corridos e cobrancas apos vencimento.
- Conferir a criacao do Evento, envio do e-mail, acesso pelo link, upload de documentos, disponibilidade em `Discussao` > `Comentarios` e localizacao por `Todos os Eventos` e `Eventos Relacionados`.
- Testar `Solicitar Mais Informacoes do Terceiro`, preservando respostas anteriores, documentos recebidos, solicitacoes feitas e historico do dossie.
- Validar Background Check com Data Engine e `Nenhuma`, tratando custo, resultado, disponibilidade, dados pessoais e permissao de consulta como pontos separados.
- Para `Contratado`, testar pontuacao, risco, data inicial, periodicidade e `Iniciar Revisao Periodica`, incluindo novos ciclos, alteracao de periodicidade, rescisao e rejeicao.
- Confirmar com produto, Compliance, seguranca e privacidade os perfis autorizados, questionarios vigentes, regras de risco e pontuacao, limites de anexos, prazos, reenvios, notificacoes, retencao, auditoria, custos do Data Engine e tratamento de falhas no portal do Terceiro.

### Prorrogacao de Prazos em Due Diligence

Com base no artigo [Prorrogacao de Prazos em Due Diligence](https://intercom.help/compliasset/pt-BR/articles/4360593-prorrogacao-de-prazos-em-due-diligence), publicado em 5 de dezembro de 2024:

- o prazo para resposta da Due Diligence e definido em dias corridos e pode ser alterado depois que o processo for iniciado;
- o usuario acessa `Todos os Terceiros`, localiza o Terceiro, abre o perfil e consulta a secao `Eventos Relacionados`;
- o Evento de Due Diligence cujo prazo sera alterado deve ser aberto pelo titulo;
- dentro do dossie, a acao `Editar` permite informar o novo valor em `Prazo para resolucao`;
- durante a mesma edicao, outros campos e informacoes do Evento tambem podem ser ajustados;
- a alteracao e concluida pela acao `Atualizar Evento`.

#### Como essa regra deve orientar um card

- Registrar Terceiro, Evento de Due Diligence, prazo anterior e novo, unidade em dias corridos, usuario executor, motivo, data, demais campos alterados e resultado da atualizacao.
- Validar o caminho `Todos os Terceiros` > perfil > `Eventos Relacionados` > titulo do Evento > `Editar` > `Prazo para resolucao` > `Atualizar Evento`.
- Testar aumento e reducao do prazo, prazo vencido, prazo em andamento, novo prazo invalido e alteracoes simultaneas em outros campos, preservando o dossie e os documentos ja recebidos.
- Conferir o efeito da prorrogacao sobre cobrancas, notificacoes, acesso do Terceiro, status do Evento, revisoes periodicas e historico, sem criar um novo Evento ou apagar o prazo anterior.
- Confirmar com produto e Compliance os perfis autorizados, limites e formato do prazo, regra para prazos vencidos, calculo de dias corridos, auditoria, notificacoes, reenvio do link e comportamento em DDQ inicial ou periodica.

### Cadastro de Fundos

Com base no artigo [Cadastro de Fundos](https://intercom.help/compliasset/pt-BR/articles/4582372-cadastro-de-fundos), publicado em 6 de outubro de 2025:

- o cadastro pode ser iniciado em `Fundos` > `Novo Fundo` ou em `Todos os Fundos` > `+`;
- `CNPJ`, nome e risco sao obrigatorios;
- tambem podem ser informados familia/estrategia, data de criacao, data de fechamento, termino do prazo de investimento, gestor responsavel, administrador, observacao e Grupo;
- `Confirmar` salva o cadastro;
- Fundos com data de fechamento passada aparecem na aba `Desativados`;
- a listagem permite filtrar por familia/estrategia e gestor, pesquisar pela lupa e exportar pela acao `Exportar`.

#### Como essa regra deve orientar um card

- Registrar Fundo, CNPJ, nome, risco, estrategia, datas, gestor, administrador, Grupo, usuario, acao e resultado.
- Validar campos obrigatorios, datas, vinculo a Grupo, `Confirmar`, filtros, busca, exportacao e transicao para `Desativados`.
- Confirmar com produto a regra de fechamento, permissoes, validacao de CNPJ, comportamento de datas futuras e passadas, custos, auditoria e retencao.

### Upload de Novos Fundos

Com base no artigo [Upload de Novos Fundos](https://intercom.help/compliasset/pt-BR/articles/7903584-upload-de-novos-fundos), publicado em 14 de agosto de 2023:

- o upload ocorre em `Fundos` > `Todos os Fundos` > `+` > `Importar uma Lista de Fundos`;
- o modelo usa `Nome`, `Familia / Estrategia`, `CPF/CNPJ`, `Criado em`, `Data de fechamento`, `Termino do prazo de investimento`, `Administrador` e `Observacao`;
- `Nome` e CPF/CNPJ sao obrigatorios; a primeira linha deve ser mantida e os dados comecam na segunda;
- campos opcionais podem ficar vazios com virgulas consecutivas (`,,`);
- o arquivo deve ser `.csv`, com campos separados por virgulas;
- `Importar` exibe simulacao e `Criar/Atualizar Fundos` confirma a carga.

#### Como essa regra deve orientar um card

- Validar modelo, ordem das colunas, CSV, campos obrigatorios, datas, campos vazios, simulacao e confirmacao.
- Registrar linhas criadas ou atualizadas, erros, duplicidades, identificador, arquivo, usuario, permissao e resultado sem expor CNPJ ou dados pessoais completos.
- Confirmar identificacao de registros existentes, limite, processamento parcial ou rollback, auditoria e efeitos em Grupos e Eventos.

### Reenvio de Due Diligence para Terceiros

Com base no artigo [Reenvio de Due Diligence para Terceiros](https://intercom.help/compliasset/pt-BR/articles/12961469-reenvio-de-due-diligence-para-terceiros), publicado em 28 de novembro de 2025:

- no perfil do Terceiro, o Evento de Due Diligence fica em `Eventos Relacionados`;
- ao abrir o Evento, `Reenviar lembrete` dispara novamente o e-mail com as informacoes de acesso e o prazo de resposta;
- todos os reenvios ficam registrados no Historico do Evento.

#### Como essa regra deve orientar um card

- Registrar Terceiro, Evento, usuario, data, motivo, destinatario, prazo vigente, quantidade de reenvios, entrega e resultado, sem armazenar link ou token.
- Validar `Eventos Relacionados`, titulo do Evento, `Reenviar lembrete`, mensagem, prazo, duplicidade de envio e Historico.
- Confirmar com produto e seguranca perfis autorizados, limites, intervalo de reenvio, auditoria, protecao contra abuso e efeitos sobre cobrancas.

### Upload de Novos Terceiros

Com base no artigo [Upload de Novos Terceiros](https://intercom.help/compliasset/pt-BR/articles/8260556-upload-de-novos-terceiros), publicado em 15 de agosto de 2023:

- o upload ocorre em `Terceiros` > `Todos os Terceiros` > `+` > `Importar uma Lista de Terceiros`;
- o modelo usa `Tipo Parceiro`, `Razao Social / Nome Completo`, `Nome Fantasia`, `CPF/CNPJ/Passaporte/RNE`, `E-mail`, `CEP`, `Endereco`, `Numero`, `Complemento`, `Estado`, `Cidade`, `Pais` e `Risco`;
- sao obrigatorios Razao Social/Nome, documento, E-mail, CEP, Endereco, Numero, Estado, Cidade e Pais;
- os codigos de pessoa sao `1`, `2` e `3`, e os de risco sao `1`, `2`, `3` e `0`;
- a primeira linha deve ser mantida, campos vazios usam `,,` e o arquivo deve ser `.csv`;
- a simulacao ocorre depois de `Importar` e a confirmacao ocorre por `Criar/Atualizar Terceiros`.

#### Como essa regra deve orientar um card

- Validar modelo, obrigatoriedade, códigos, CSV, campos vazios, simulacao e confirmacao.
- Testar documentos CPF/CNPJ/Passaporte/RNE, duplicidades, dados invalidos, processamento parcial, permissao, auditoria e efeitos em Due Diligence e Eventos.
- Confirmar chave de identificacao, limites, codificacao, tratamento de Passaporte/RNE, mensagens de erro e retencao do arquivo.

### Cadastro de Terceiros

Com base no artigo [Cadastro de Terceiros](https://intercom.help/compliasset/pt-BR/articles/8257454-cadastro-de-terceiros), publicado em 30 de setembro de 2025:

- o cadastro ocorre em `Terceiros` > `Novo Terceiro` ou em `Todos os Terceiros` > `+`;
- deve-se selecionar Pessoa Juridica, Pessoa Fisica ou Estrangeiro e preencher os campos obrigatorios correspondentes;
- o cadastro pode conter data de entrada, telefone, categoria e, para Pessoa Juridica, pessoa de contato;
- `Adicionar nova categoria`, lapis e lixeira permitem gerir categorias;
- `Criar Terceiro` salva o registro;
- o perfil apresenta dados gerais, painel de Due Diligence, `Eventos Relacionados`, Dossie Reputacional do Data Engine e `Discussao`;
- Terceiros podem ser incluidos em Grupos para selecao em Eventos;
- o CNPJ aceita formato alfanumerico conforme a regra anunciada para 2026.

#### Como essa regra deve orientar um card

- Registrar tipo de pessoa, documento, nome, e-mail, endereco, contato, categoria, data de entrada, Grupo, usuario, acao e resultado.
- Validar campos dependentes do tipo, categoria, `Criar Terceiro`, edicao, Due Diligence, Eventos, Dossie Reputacional e Discussao.
- Confirmar regra de CNPJ alfanumerico, validacoes, permissoes, filtros, retencao e efeitos de categorias e Grupos em Eventos.

### Diferenca entre Dossie Reputacional e Due Diligence de Terceiros

Com base no artigo [Diferenca entre Dossie Reputacional e Due Diligence de Terceiros](https://intercom.help/compliasset/pt-BR/articles/8429615-diferenca-entre-dossie-reputacional-e-due-diligence-de-terceiros), publicado em 29 de abril de 2026:

- o Dossie Reputacional do Data Engine e uma consulta externa baseada em nome e CPF/CNPJ, disponivel em dossies e perfis de Relacionados;
- o artigo informa custo de R$15 para CPF e R$25 para CNPJ, com retorno em alguns minutos, valores que devem ser confirmados antes de uso comercial;
- Due Diligence de Terceiros e um processo de investigacao anterior a contrato ou acordo financeiro;
- a DD pode usar Background Check do Data Engine, mas essa consulta e opcional e nao substitui o questionario;
- a DD tambem pode usar sete questionarios da Anbima ou questionario proprio da Biblioteca de Documentos;
- Dossie Reputacional e consulta pontual; Due Diligence inclui questionario, documentos, avaliacao, risco e acompanhamento do Terceiro.

#### Como essa regra deve orientar um card

- Classificar a demanda como consulta reputacional ou Due Diligence antes de definir fluxo, permissao, evidencia e criterio de aceite.
- Registrar nome, documento mascarado, origem, finalidade, custo informado, resultado, questionario, documentos, risco e decisao, sem expor dados pessoais completos.
- Validar que uma consulta do Data Engine pode integrar a DD, mas nao substitui questionario, documentos, avaliacao ou historico do processo.
- Confirmar com produto, juridico, seguranca e privacidade custos, perfis autorizados, escopos, retencao, auditoria e tratamento de erro ou retorno incompleto.

### Guia de primeiros passos

Com base no artigo [Guia de Primeiros Passos](https://intercom.help/compliasset/pt-BR/articles/8727731-guia-de-primeiros-passos), publicado em 21 de dezembro de 2023, o roteiro abaixo e uma recomendacao de onboarding, e nao uma sequencia obrigatoria de uso do sistema:

1. **Login:** acessar `Acesso de Clientes`, escolher `Empresas` ou `EFPC`, informar e-mail cadastrado e senha temporaria recebida no e-mail de boas-vindas ou usar Google e Office 365.
2. **Criacao e distribuicao dos times:** cadastrar Colaboradores manualmente em `Colaboradores` > `Novo Colaborador` ou por planilha e, depois, organiza-los em Grupos, Departamentos ou Funcoes em `Configuracoes`.
3. **Atribuicao de tarefas:** definir os acessos, revisar Atividades da Agenda e Obrigacoes Estruturais, arquivar o que nao se aplica a empresa, criar Atividades e Obrigacoes adicionais quando necessario, ajustar prazos das Atividades e atribuir responsaveis.
4. **Informacoes extras:** cadastrar Fundos, Investidores e Terceiros manualmente ou por planilha e adicionar documentos essenciais, como atas, politicas e manuais, a biblioteca de `Documentos`.
5. **Inicio da operacao:** executar Atividades e Obrigacoes, criar Eventos e iniciar Campanhas de Treinamentos, Aceites de Documentos ou Formularios para os Colaboradores.

#### Como esse roteiro deve orientar um card

- Tratar o roteiro como referencia de onboarding e nunca como pre-requisito universal para uso de uma funcionalidade ou para aceite de uma entrega.
- Registrar a etapa de onboarding, empresa ou ambiente, dados carregados, perfis e responsaveis definidos, itens revisados ou arquivados e pendencias que impedem o inicio operacional.
- Para inclusao de dados, separar Colaboradores, Fundos, Investidores, Terceiros e Documentos, aplicando a regra especifica de cadastro, importacao, permissao e acesso de cada modulo.
- Para a revisao inicial da Agenda e das Obrigacoes Estruturais, distinguir arquivamento de exclusao e preservar a justificativa, o responsavel e a evidencia da decisao sobre cada item.
- Para o inicio de Campanhas, registrar modulo, publico e acao esperada; nao assumir que a regra de inclusao de novos Colaboradores apos o inicio e identica em Treinamentos, Aceites e Formularios.
- Confirmar com produto e implantacao os passos obrigatorios por plano ou ambiente, o fluxo atual de acesso para Empresas e EFPC, permissoes de carga inicial, regras de arquivamento e os requisitos minimos para considerar um ambiente operacionalmente pronto.

### Cartoes regulatorios do Dashboard

Com base no artigo [Novos Cartoes no Dashboard](https://intercom.help/compliasset/pt-BR/articles/7173226-novos-cartoes-no-dashbord), publicado em 22 de março de 2023:

- o cartao `Modulos Regulatorios` apresenta os modulos contratados pela empresa que compoem sua Agenda Regulatoria, como Gestor de Recursos, Gestor de Carteiras Administradas, Administrador Fiduciario e DTVM;
- para cada modulo, o grafico informa a quantidade de Atividades por status: `Em Aberto`, `Em Andamento`, `Concluido` e `Nao Realizado`;
- ao posicionar o cursor sobre uma cor do grafico, o sistema apresenta numero e percentual do status de evolucao correspondente;
- o periodo pode ser filtrado, inclusive para anos anteriores, pelo seletor apresentado como `01/2023 - Hoje`;
- o cartao `Categorias por Modulos` apresenta categorias ou normativos de cada modulo e seus status acumulados; a navegacao ocorre ao selecionar o nome do modulo desejado;
- o mesmo filtro de periodo e disponibilizado em `Categorias por Modulos`;
- os dois cartoes podem ser exibidos ou ocultados pelo botao com icone de olho, selecionando os cartoes desejados.

#### Como essa regra deve orientar um card

- Registrar empresa ou ambiente, cartao, modulo, categoria, periodo, dados agregados por status, interacao de detalhamento e estado de visibilidade do cartao.
- Tratar o Dashboard como visao agregada da Agenda Regulatoria: validar que totais e percentuais correspondem aos dados de origem, sem permitir que a exibicao altere Atividades ou seus status.
- Para filtros, testar periodo padrao e anos anteriores em ambos os cartoes, garantindo que todos os totais, percentuais, categorias e detalhamentos usem o mesmo recorte temporal.
- Validar o detalhamento exibido pelo cursor para cada status e preservar a consistencia de arredondamento entre contagem e percentual.
- Para o icone de olho, testar exibicao e ocultacao por cartao, persistencia da preferencia e ausencia de impacto nos dados, permissoes ou demais cartoes.
- Confirmar com produto a lista vigente de modulos contratados, definicao de categoria, regras de calculo de status e percentual, filtros disponiveis, comportamento de visibilidade, permissao de configuracao e diferencas da versao atual do Dashboard.

### Cartoes operacionais do Dashboard

Com base no artigo [Navegando pelo Dashboard](https://intercom.help/compliasset/pt-BR/articles/7125299-navegando-pelo-dashboard), publicado em 24 de junho de 2024:

- o Dashboard apresenta em cartoes informacoes que ja existem no sistema e pode ser customizado com inclusao, ocultacao e reposicionamento dos cartoes relevantes;
- `Calendario` usa dados da Agenda, Obrigacoes Estruturais e Eventos para mostrar as tarefas do mes, incluindo itens concluidos, em aberto e atrasados;
- `Risco de Eventos Mapeados` apresenta graficamente os riscos de Eventos por status; as cores indicadas sao vermelho para risco alto, amarelo para medio, verde para baixo e preto para `N/A`;
- `Eventos Frequentes` exibe as naturezas de Eventos mais usadas por indice de ocorrencia e permite consultar anos anteriores e Relacionados com maior frequencia;
- `Eventos Pendentes` lista Eventos ainda nao realizados, organizados pelo prazo maximo de conclusao; os indicadores circulares mostram a cor de risco de cada Evento;
- `Atividades e Eventos Cumpridos` e um grafico de linhas com a quantidade de Atividades e Eventos realizados e o mes de conclusao;
- `Campanhas de Aceite de Documentos` apresenta campanhas de aceite que circularam no sistema, com data de envio e titulo;
- `Eventos Nao Categorizados` disponibiliza um endereco de e-mail para criacao de Evento fora do sistema; depois do envio, o Evento aparece no cartao e pode receber informacoes adicionais;
- `Atividades Vencidas` apresenta Atividades que atingiram o prazo maximo de conclusao; elas continuam podendo ser realizadas, deixando o cartao atualizado apos a conclusao;
- `Categorias por Modulos` e `Modulos Regulatorios` complementam o acompanhamento da Agenda e dos modulos contratados, conforme as regras de cartoes regulatorios deste guia;
- os cartoes descritos sao criados automaticamente pelo sistema; cartoes adicionais seguem o fluxo de filtros documentado em `Personalizacao do Dashboard`.

#### Como essa regra deve orientar um card

- Registrar cartao, usuario, ambiente, dados de origem, periodo, status, risco, ordenacao e resultado esperado, distinguindo cartao operacional de cartao regulatorio ou criado por filtro.
- Validar que cada cartao reflete seus dados de origem sem altera-los: Agenda e Eventos para Calendario, riscos dos Eventos para os cartoes de risco e pendencia, e campanhas de Aceite para o cartao de campanhas.
- Para cores de risco, testar alto, medio, baixo e `N/A` e validar que os indicadores de `Eventos Pendentes` correspondem ao risco do Evento relacionado.
- Para `Eventos Nao Categorizados`, registrar apenas identificadores seguros e o resultado da criacao; nao expor o endereco completo de criacao por e-mail, dados sensiveis enviados ou conteudo do Evento em evidencias de card.
- Para `Atividades Vencidas`, validar que a conclusao posterior ao prazo atualiza o cartao e preserva datas, status e historico de atraso, sem ocultar o fato de que o vencimento foi ultrapassado.
- Ao abrir detalhes a partir de qualquer cartao, aplicar as permissoes e o recorte correspondente; o Dashboard nao deve ampliar acesso aos Eventos, Atividades, campanhas ou dossies.
- Confirmar com produto a lista vigente de cartoes padrao, fontes de dados, ordenacao, calculo de pendencia e cumprimento, semantica das cores, endereco e regras de criacao de Eventos por e-mail, atualizacao apos conclusao e permissoes por perfil.

### Calendario do Dashboard

Com base no artigo [Tour pelo Calendario do Dashboard](https://intercom.help/compliasset/pt-BR/articles/8576396-tour-pelo-calendario-do-dashboard), publicado em 4 de abril de 2025:

- o cartao `Calendario`, localizado a esquerda no Dashboard, inicia no mes e ano correntes e pode navegar para periodos passados e futuros conforme vencimentos e prazos de resolucao;
- o Calendario agrega demandas da Agenda, Obrigacoes Estruturais e Eventos;
- as cores de status sao verde para itens concluidos, amarelo para itens em aberto dentro do prazo e vermelho para itens em atraso;
- ao selecionar uma data, o usuario visualiza as tarefas daquele dia com prazo de resolucao, titulo e responsavel, quando houver;
- para a data selecionada, o filtro `Responsavel(is)` exibe os dossies atribuidos ao Colaborador escolhido que tenham vencimento naquele dia;
- o filtro por responsavel exige atribuicao previa do Colaborador no dossie; a borda dos itens indica seu status atual;
- ao selecionar o titulo de uma tarefa, o sistema abre o dossie correspondente para inclusao de evidencias e conclusao da demanda;
- `Ver Todas` permite escolher a secao a consultar entre Agenda, Eventos e Obrigacoes Estruturais.

#### Como essa regra deve orientar um card

- Registrar usuario, ambiente, mes e ano, data selecionada, secao de origem, tarefa, prazo, responsavel, status, cor e resultado da navegacao para o dossie.
- Validar a navegacao entre periodos, o carregamento inicial no mes e ano correntes e a inclusao coerente de Agenda, Obrigacoes Estruturais e Eventos de acordo com seus prazos.
- Testar as cores verde, amarelo e vermelho contra o status e prazo reais, distinguindo item em aberto dentro do prazo de item atrasado.
- Para o filtro `Responsavel(is)`, validar que so retorna dossies atribuidos previamente ao Colaborador e com vencimento na data selecionada, sem expor tarefas sem permissao.
- Ao abrir uma tarefa ou usar `Ver Todas`, preservar a secao, data e filtros compativeis e aplicar as permissoes de acesso ao dossie e a lista de destino.
- Confirmar com produto a definicao de datas para Agenda, Obrigacoes e Eventos, regras de status e cores, localizacao do cartao, comportamento de periodos futuros, combinacao de filtros, escopo de `Ver Todas` e persistencia de selecao.

### Personalizacao do Dashboard

Com base no artigo [Customizando o Dashboard](https://intercom.help/compliasset/pt-BR/articles/2047898-customizando-o-dashboard), publicado em 1 de agosto de 2024:

- o Dashboard pode ser personalizado individualmente por cada Membro do time de Compliance para priorizar a visualizacao de pendencias e informacoes apos o login;
- os cartoes podem ser reorganizados ao selecionar, manter pressionado e arrastar o cartao para a posicao desejada;
- um cartao pode ser ocultado pelo botao `x` no canto superior direito;
- o icone de olho no canto superior direito do Dashboard exibe os cartoes disponiveis e permite habilita-los ou desabilita-los novamente;
- o cartao `Eventos Frequentes` permite filtrar por ano e consultar as naturezas de Eventos mais usadas no periodo;
- em `Eventos Frequentes`, selecionar o titulo altera para o filtro `Relacionados Frequentes`, que lista Colaboradores e a quantidade de Eventos em que cada um aparece como Envolvido;
- para consultar detalhes, o usuario deve selecionar os dados apresentados nos cartoes;
- a exibicao em `Relacionados Frequentes` e apenas informativa sobre quantidade de Eventos relacionados e nao representa avaliacao negativa do Colaborador;
- novos cartoes podem ser criados a partir de filtros de `Agenda` > `Todas as Atividades` e `Eventos` > `Todos os Eventos`;
- no filtro de Atividades, estao disponiveis Recorrencia, Responsavel(eis), Categoria(s), Assunto(s), Modulo e as classificacoes prazo fixo, novas, alteradas e proprias;
- apos definir os filtros, `Adicionar ao Dashboard` solicita o titulo do cartao e `Confirmar` o adiciona ao Dashboard;
- um cartao criado por filtro de Atividades exibe as cinco primeiras Atividades do resultado; `Ver mais` abre o resultado completo e o `x` remove o cartao do Dashboard;
- o fluxo para criar cartao por filtro de Eventos segue os mesmos passos em `Eventos` > `Todos os Eventos`.

#### Como essa regra deve orientar um card

- Registrar usuario, ambiente, cartao, ordem anterior e nova, estado de visibilidade, filtros aplicados e dados apresentados, separando preferencia individual de configuracao global do Dashboard.
- Testar arrastar e soltar para reorganizacao, ocultacao pelo `x` e reativacao pelo icone de olho, incluindo persistencia apos recarregamento, nova sessao e troca de ambiente quando aplicavel.
- Para `Eventos Frequentes`, validar filtro por ano e o detalhamento das naturezas; para `Relacionados Frequentes`, validar o filtro alternativo, o vinculo dos Eventos com os Colaboradores e a contagem exibida.
- Para cartoes criados por filtro, registrar modulo de origem, filtros, titulo, usuario, ambiente, data de criacao, total de resultados e as cinco Atividades exibidas na previa quando aplicavel.
- Testar os filtros de Agenda e Eventos, a inclusao por `Adicionar ao Dashboard` e `Confirmar`, a exibicao de cinco Atividades, `Ver mais` com o resultado completo e a remocao pelo `x`.
- Garantir que alterar ordem, filtro ou visibilidade nao modifique Eventos, naturezas, Relacionados, permissoes ou dados de outros usuarios.
- Ao abrir detalhes por um dado do cartao, aplicar as permissoes vigentes e o mesmo recorte de filtro; o Dashboard nao deve conceder acesso adicional a registros ou dossies.
- Confirmar com produto a elegibilidade de personalizacao por perfil, persistencia entre dispositivos, comportamento em cartoes removidos ou indisponiveis, filtros disponiveis, criterios de `Eventos Frequentes` e `Relacionados Frequentes`, efeitos da edicao ou exclusao de filtros de origem e limites de criacao de cartoes.

## Como usar artigos e materiais de referencia

A ideia de reunir os artigos e boa, desde que eles sejam organizados como base de conhecimento e nao apenas anexados em massa.

Priorize nesta ordem:

1. artigos oficiais e documentacao atual do CompliAsset;
2. artigos que explicam fluxos, modulos, perfis, regras e limites do sistema;
3. artigos sobre erros, configuracoes, integracoes e comportamentos conhecidos;
4. materiais internos, atas e exemplos reais de uso;
5. referencias antigas, sempre identificadas como historicas.

Para cada material incorporado, registre:

- titulo;
- link ou caminho do arquivo;
- modulo ou assunto;
- data de consulta;
- se esta vigente, historico ou pendente de confirmacao;
- quais regras do sistema ele comprova.

Nao trate um artigo como verdade absoluta quando ele estiver desatualizado, contraditorio ou descrever uma configuracao especifica de um cliente. Nesses casos, abrir uma demanda de investigacao ou marcar a informacao como pendente de validacao.

Recomendacao pratica: enviar os artigos em lotes por tema, com um indice. Comece pelos fluxos basicos e modulos mais usados; depois inclua excecoes, integracoes e materiais de suporte. Isso facilita a consulta e reduz o risco de uma regra antiga orientar um card novo.

## Estado da consolidacao da base

Os materiais incorporados formam uma base de trabalho, e nao uma especificacao definitiva: todos os artigos no indice estao como `Vigente a confirmar` ate que Produto, Seguranca, Suporte ou a versao atual do sistema validem a regra aplicavel.

Enquanto novos artigos forem incorporados, aplique os seguintes criterios:

1. Preserve o fato e o link de cada fonte, mesmo quando houver divergencia.
2. Prefira a fonte mais recente e mais especifica para orientar uma investigacao, sem promover sua regra a criterio de aceite antes da validacao.
3. Quando duas fontes tratarem a mesma regra de formas diferentes, abra ou vincule uma demanda de investigacao em vez de escolher uma delas por inferencia.
4. Mantenha regras de seguranca, privacidade, historico e permissao restritivas ate haver confirmacao contraria documentada.

### Divergencias e pontos de consolidacao conhecidos

- **Dominio de Previdencia:** `FAQ de acesso e login` referencia `abrapp.compliasset.com`, enquanto `Orientacoes para redefinicao de senha` referencia `previ.compliasset.com`. A lista oficial de ambientes precisa ser confirmada antes de orientar login ou recuperacao.
- **Desbloqueio de acesso:** o FAQ atribui a acao ao time de compliance, enquanto o artigo de desbloqueio descreve acao por Administrador e desbloqueio automatico em 24 horas. Confirmar responsavel, prazo e notificacoes.
- **Visibilidade de documentos:** a FAQ da Biblioteca menciona todos os Colaboradores cadastrados, e o artigo especifico menciona Colaboradores ativos. Tratar como pendente a elegibilidade exata de usuarios desligados, bloqueados ou sem primeiro acesso.
- **Matriz de permissoes:** a tabela de Usuario x Administrador foi publicada em 2023 e e a fonte mais granular para criar, editar, excluir e arquivar. As descricoes posteriores de perfil sao contextuais; qualquer divergencia deve ser validada antes de alterar a matriz.
- **Configuracoes e permissao administrativa:** o guia registra que `Configuracoes` e exclusiva de Membro-Administrador, mas alguns artigos usam apenas o termo Administrador. Confirmar quando o termo inclui ou diferencia Super Administrador e Membro-Administrador.

## Regras de seguranca documentadas

### Canais de ajuda e atendimento

Com base no artigo [Canais de Ajuda](https://intercom.help/compliasset/pt-BR/articles/6826944-canais-de-ajuda), publicado em 23 de abril de 2026:

- o chat da aplicacao e o principal canal para duvidas e solicitacoes e pode ser acessado dentro ou fora do sistema, sem necessidade de login;
- o atendimento por chat e por `suporte@compliasset.com` ocorre de segunda a sexta-feira, das 9h as 18h, no horario de Brasilia;
- a `Central de Ajuda`, acessivel pelo menu lateral, organiza artigos por colecoes, permite pesquisa por temas e titulos e sugere leituras relacionadas ao fim de cada artigo;
- quando o usuario avalia negativamente um artigo da Central de Ajuda, o sistema abre automaticamente um novo chat com o suporte;
- as noticias, incluindo Boletins Diarios, Alertas Regulatorios e notas de atualizacao, podem ser acessadas pelo chat e avaliadas ao final;
- as notas de atualizacao e correcoes podem ser acessadas pelo icone de chat, na secao `Noticias`, ou pelo link externo disponibilizado pelo CompliAsset;
- comunicacoes de correcoes sao publicadas mensalmente, enquanto atualizacoes sao publicadas quando uma nova funcionalidade e disponibilizada no sistema;
- o CompliAsset disponibiliza treinamentos gravados por perfil de acesso e informa que treinamentos ao vivo e sessoes de tira-duvidas podem ser agendados com o suporte, sem custo adicional.

#### Como essa regra deve orientar um card

- Direcionar duvidas de usabilidade, incidentes e solicitacoes de suporte ao chat ou a `suporte@compliasset.com`, registrando o contexto minimo, ambiente, passos, evidencias sem dados sensiveis e identificador do atendimento.
- Usar a Central de Ajuda como fonte de referencia, mas manter a validacao de vigencia antes de converter um artigo em requisito de produto ou criterio de aceite.
- Para falhas no feedback de artigo, testar a avaliacao negativa e a abertura do chat sem expor o conteudo de conversas, dados pessoais ou historico de atendimento a usuarios nao autorizados.
- Para noticias e treinamentos, registrar perfil, canal de acesso, conteudo ou sessao solicitada e resultado, sem pressupor que todas as noticias ou treinamentos estao disponiveis a todos os perfis.
- Para notas de atualizacao, diferenciar correcao de nova funcionalidade, registrar data de publicacao, versao ou funcionalidade afetada quando disponivel e nao presumir que uma publicacao esgota todas as alteracoes realizadas no periodo.
- Nao tratar horario de atendimento, gratuidade, chamadas de video ou treinamento ao vivo como SLA ou condicao contratual sem confirmacao comercial e de suporte vigente.
- Confirmar com suporte e comercial o horario e abrangencia dos canais, funcionamento do chat sem login, regras de abertura automatica, retencao de conversas e feedback, disponibilidade por perfil, cadencia e escopo de notas de atualizacao e condicoes de agendamento e custo dos treinamentos.

### Visao geral de Configuracoes

Com base no artigo [Explorando 'Configuracoes'](https://intercom.help/compliasset/pt-BR/articles/8985454-explorando-configuracoes), publicado em 27 de fevereiro de 2024:

- `Configuracoes`, identificada pelo icone de engrenagem no fim do menu lateral, e restrita a Membros-Administradores pela sensibilidade dos dados e controles disponiveis;
- `Auditoria` centraliza o Historico de Acessos com data, usuario, IP, cidade, estado, pais, versao e origem, e permite consultar de forma agrupada os dossies reputacionais ja consultados;
- `Membros` permite transformar Colaboradores em Membros, alterar perfis e definir acessos;
- `Grupos`, `Departamentos` e `Funcoes` apoiam a segmentacao de Relacionados e dos perfis de Colaboradores;
- `Visual` personaliza logotipo e cores dos canais de Compliance, LGPD e Denuncias;
- `Canais` permite definir responsaveis pelo recebimento das demandas enviadas por funcionarios ou usuarios externos e personalizar links externos relacionados;
- `Naturezas de Eventos` permite criar novas naturezas e definir quais ficam visiveis para Membros e Colaboradores; o artigo informa que o sistema disponibiliza mais de 100 naturezas;
- `API` fornece tokens para integracao segura com aplicativos e servicos externos;
- `Seguranca` permite configurar a expiracao periodica de senhas.

#### Como essa regra deve orientar um card

- Registrar o modulo de Configuracoes afetado, empresa ou ambiente, Membro-Administrador responsavel, configuracao anterior e nova, justificativa, data de publicacao ou confirmacao e impacto nos usuarios e integracoes.
- Restringir todos os submodulos de Configuracoes a Membros-Administradores e testar o bloqueio para Membros-Usuarios e Colaboradores por menu, URL direta, API e sessao ativa.
- Para Auditoria, diferenciar Historico de Acessos e consulta de dossies reputacionais; validar os campos adicionais de `Versao` e `Origem` sem presumir seus valores, formato ou retencao.
- Para Canais, registrar canal, responsaveis, link externo e publico afetado; nao assumir regras de distribuicao, anonimato, permissao ou retencao sem a documentacao especifica do canal.
- Para Naturezas de Eventos, registrar natureza criada ou alterada, visibilidade por perfil e impactos em Eventos existentes; nao presumir que todas as mais de 100 naturezas padrao podem ser editadas ou excluidas.
- Aplicar as regras especificas deste guia para Membros, Grupos, Visual, tokens de API e expiracao de senha; esta visao geral nao substitui seus criterios de permissao, seguranca e auditoria.
- Confirmar com produto e seguranca a lista vigente de submodulos, permissao de cada um, significado de versao e origem na Auditoria, gestao de dossies reputacionais, regras de Canais e o ciclo de vida, limite e visibilidade das Naturezas de Eventos.

### Configuracao visual dos canais e comunicacoes

Com base no artigo [Explorando a Secao 'Visual'](https://intercom.help/compliasset/pt-BR/articles/7947430-explorando-a-secao-visual), publicado em 3 de abril de 2025:

- um Membro-Administrador acessa `Configuracoes` > `Visual` para personalizar a identidade visual da empresa;
- o logotipo aceita arquivos PNG, JPG ou GIF, com dimensoes maximas de 300 por 50 pixels;
- a `Cor de fundo` e aplicada ao cabecalho dos canais e a outros fundos do sistema;
- a `Cor de realce` e aplicada aos botoes dos canais e a outros elementos de destaque;
- a acao `Definir e Publicar` salva e publica a configuracao;
- a personalizacao e refletida nos canais de Compliance, Denuncia e LGPD, nos PDFs de campanhas e nas notificacoes por e-mail enviadas pelo sistema;
- um Membro-Administrador pode alterar essas configuracoes a qualquer momento, e a alteracao deve ser refletida automaticamente nos canais e comunicacoes citados.

#### Como essa regra deve orientar um card

- Registrar a empresa ou ambiente afetado, o Membro-Administrador responsavel, os valores anteriores e novos, os canais e comunicacoes impactados e o momento da publicacao.
- Para upload de logotipo, validar formato, dimensoes maximas e mensagens de erro; nao assumir limites de tamanho em bytes, tratamento de transparencia ou comportamento de animacao do GIF sem confirmacao.
- Diferenciar rascunho, se existir, de configuracao publicada: somente o resultado de `Definir e Publicar` deve ser tratado como a alteracao com efeito nos canais, PDFs e e-mails.
- Para falhas de propagacao, verificar separadamente os canais de Compliance, Denuncia e LGPD, PDFs de campanhas e notificacoes por e-mail, sem supor que todos compartilham o mesmo mecanismo de renderizacao.
- Restringir criacao, alteracao e publicacao da identidade visual ao Membro-Administrador; demandas para outros perfis devem explicitar a revisao de permissao e seu impacto.
- Considerar auditoria da alteracao, inclusive responsavel, data, horario, configuracao anterior e nova e resultado da publicacao, sem armazenar arquivos de marca desnecessariamente em evidencias de card.
- Confirmar com produto, design e tecnologia os limites em bytes, formatos e dimensoes efetivamente processados, acessibilidade e contraste das cores, existencia de pre-visualizacao ou rascunho, reversao, historico, escopo por ambiente e prazo de propagacao para PDFs e e-mails.

### Pessoas de contato do Canal de Compliance

Com base no artigo [Alteracao de Pessoa de Contato](https://intercom.help/compliasset/pt-BR/articles/9949044-alteracao-de-pessoa-de-contato), publicado em 7 de outubro de 2024:

- na visao de Membro, um Membro-Administrador acessa `Configuracoes` > `Canal de Compliance` para definir as pessoas de contato do time de compliance;
- no campo `Destinatario(s)`, pode-se definir uma ou mais pessoas de contato, cujo nome completo e e-mail sao exibidos na visao do Colaborador;
- a acao `Definir e Publicar` confirma e publica a alteracao;
- as pessoas definidas devem ser conferidas no painel de controle da visao do Colaborador;
- as pessoas de contato recebem notificacao por e-mail quando um novo Evento e criado pelo Canal de Compliance ou pela visao do Colaborador;
- o Super Administrador e incluido automaticamente como pessoa de contato, mas pode ser substituido.

#### Como essa regra deve orientar um card

- Registrar canal, empresa ou ambiente, pessoas de contato anteriores e novas, Membro-Administrador responsavel, acao de publicacao, resultado na visao do Colaborador e notificacoes geradas.
- Restringir a alteracao de `Destinatario(s)` ao Membro-Administrador e validar o bloqueio por interface, URL direta, API e sessao ativa para Membros-Usuarios e Colaboradores.
- Testar uma e varias pessoas de contato, a exibicao de nome e e-mail no painel do Colaborador e a atualizacao somente apos `Definir e Publicar`.
- Para notificacoes, validar separadamente a criacao de Evento pelo Canal de Compliance e pela visao do Colaborador, conferindo que os destinatarios publicados recebem o aviso sem expor os demais destinatarios ao solicitante.
- Diferenciar o Super Administrador como contato padrao de sua protecao contra alteracao de perfil: substituir o contato nao deve alterar o perfil, as permissoes ou a unicidade do Super Administrador.
- Confirmar com produto, seguranca e privacidade os perfis elegiveis como contato, limites de destinatarios, comportamento de adicao ou remocao do Super Administrador, escopo de notificacoes, historico, prazo de propagacao e regras dos Eventos criados em cada origem.

### Alteracao de nomes e e-mails de colaboradores

Com base no artigo [Alteracao de Nomes e E-mails de Colaboradores](https://intercom.help/compliasset/pt-BR/articles/4789039-alteracao-de-nomes-e-e-mails-de-colaboradores), publicado em 26 de abril de 2023:

- usuarios nao conseguem editar diretamente nome ou e-mail de colaboradores;
- a alteracao deve ser feita internamente pelo time do CompliAsset, depois da confirmacao do suporte;
- o e-mail so pode ser alterado quando continuar pertencendo a mesma pessoa;
- o novo e-mail nao pode estar cadastrado em outra empresa contratante do CompliAsset;
- a recomendacao geral, quando aplicavel, e criar um novo cadastro com o nome e e-mail corretos;
- depois da autorizacao do suporte, a solicitacao deve ser enviada para `suporte@compliasset.com`;
- o assunto orientado pelo artigo e `Alteracao Dominio de E-mail`;
- o corpo do e-mail deve informar claramente os valores `DE/PARA`, preferencialmente com um responsavel do time solicitante em copia.

#### Como essa regra deve orientar um card

- Nao abrir uma demanda propondo liberar a edicao direta de nome ou e-mail sem justificar e revisar o risco de seguranca, identidade e isolamento entre empresas.
- Para um ajuste individual, registrar a confirmacao do suporte, a pessoa afetada, o valor atual e o valor desejado sem expor dados desnecessarios.
- Nao assumir que o suporte pode alterar o dado: primeiro verificar se a pessoa e a mesma e se o novo e-mail nao existe em outro ambiente contratante.
- Considerar como alternativa a criacao de um novo cadastro e desativacao ou tratamento do cadastro anterior, conforme a orientacao do suporte.
- Nunca colocar senha, token ou outro segredo no card ou no e-mail de solicitacao.

#### Ponto a confirmar

O artigo apresenta uma redacao ambigua sobre a condicao para alterar o nome quando existe cadastro em mais de um ambiente. Antes de transformar essa situacao em criterio de aceite, confirmar a regra vigente com o suporte ou com a documentacao atual.

### Autenticacao de dois fatores

Com base no artigo [Autenticacao de Dois Fatores](https://intercom.help/compliasset/pt-BR/articles/1956042-autenticacao-de-dois-fatores), publicado em 2 de maio de 2023:

- a autenticacao de dois fatores adiciona uma camada extra de seguranca ao login;
- o usuario ativa a opcao pelo menu `Meu Perfil`, acessado pelo botao com sua foto ou iniciais;
- deve selecionar `Usar Autenticacao de Duas Etapas` e clicar em `Confirmar`;
- depois da ativacao, o login exige a senha e um codigo de autenticacao;
- o codigo e enviado para o e-mail cadastrado do usuario.

#### Como essa regra deve orientar um card

- Uma demanda relacionada ao login deve preservar os dois fatores quando a autenticacao estiver ativada.
- Para problemas de acesso, registrar se a senha foi aceita, se o codigo foi enviado e se o e-mail cadastrado esta acessivel.
- Nao registrar codigos de autenticacao, senhas ou tokens no card, nos anexos ou em mensagens de suporte.
- Mudancas no e-mail cadastrado devem considerar o impacto no recebimento do codigo e seguir as regras de alteracao de e-mail deste guia.
- Qualquer proposta de desligar, contornar ou alterar o segundo fator deve ser tratada como mudanca de seguranca e passar por validacao especifica.

### Configuracoes de Meu Perfil para membros

Com base no artigo [Configuracoes do Perfil](https://intercom.help/compliasset/pt-BR/articles/4360165-configuracoes-do-perfil), publicado em 22 de novembro de 2024:

- a secao `Meu Perfil` esta disponivel para todos os usuarios; este artigo documenta as configuracoes apresentadas na visao de Membro;
- o acesso ocorre pelo botao com as iniciais ou foto do usuario, ao lado das notificacoes no canto superior direito;
- nome e e-mail sao exibidos, mas nao podem ser editados nessa secao; alteracoes devem seguir o fluxo de suporte documentado neste guia;
- o usuario pode escolher o idioma do sistema entre portugues e ingles e definir a quantidade de registros exibidos por pagina;
- o artigo recomenda usar de 10 a 25 registros por pagina como referencia de experiencia e rapidez;
- o `Lembrete Semanal`, disponivel por padrao para Membros-Administradores e Membros-Usuarios, envia quando habilitado um e-mail toda segunda-feira com demandas da Agenda, Eventos e Documentos que vencem na semana, estejam ou nao atribuidas ao usuario;
- a autenticacao de duas etapas pode ser habilitada para exigir um codigo enviado por e-mail no login;
- a `Validade do Dispositivo` define a frequencia com que a senha sera solicitada novamente nos dispositivos, limitada a 60 dias;
- o usuario pode adicionar uma foto de perfil;
- a acao `Confirmar` salva uma ou mais alteracoes de configuracao.

#### Como essa regra deve orientar um card

- Registrar o perfil afetado, o campo alterado, os valores anterior e novo, o dispositivo ou navegador quando aplicavel, a confirmacao e o comportamento efetivamente persistido.
- Separar preferencias pessoais de configuracoes de seguranca: idioma, paginacao e foto nao devem ter os mesmos criterios de permissao, auditoria e validacao de autenticacao de duas etapas ou validade do dispositivo.
- Para `Lembrete Semanal`, validar destinatario Membro, segunda-feira de envio, demandas da Agenda, Eventos e Documentos que vencem na semana, itens atribuidos e nao atribuidos, fuso horario e ausencia de duplicidade.
- Para `Validade do Dispositivo`, validar limites de ate 60 dias, nova solicitacao de senha no prazo configurado, efeito em dispositivos ja confiaveis e preservacao da autenticacao de duas etapas quando estiver ativa.
- Nao propor a edicao direta de nome ou e-mail por `Meu Perfil` sem revisar as regras de identidade, unicidade, seguranca e suporte deste guia.
- Confirmar com produto e seguranca os valores de paginacao aceitos, idiomas disponiveis por ambiente, formatos e limites de foto, horario e regras do lembrete, comportamento de sessoes e dispositivos e a aplicabilidade das configuracoes na visao de Colaborador.

### Gerenciamento de notificacoes

Com base no artigo [Gerenciar as Notificacoes](https://intercom.help/compliasset/pt-BR/articles/4931000-gerenciar-as-notificacoes), publicado em 20 de junho de 2025:

- as notificacoes apresentam interacoes relacionadas ao usuario, como mencoes em comentarios de dossies dos quais ele e assinante, convites para campanhas e atribuicoes de responsabilidade em Atividades e Obrigacoes;
- a caixa de notificacoes e acessada pelo icone de sino cinza no canto superior direito, ao lado das iniciais do usuario;
- a listagem inicial exibe as ultimas 10 notificacoes recebidas em ordem cronologica; `Ver Todas` abre a listagem completa;
- uma ou mais notificacoes podem ser selecionadas e marcadas como lidas pela acao `Marcar como lidas`;
- a acao `Selecionar todas as notificacoes` permite selecionar as notificacoes da pagina ou de toda a caixa de entrada;
- o icone de envelope em uma notificacao abre o dossie relacionado;
- uma ou mais notificacoes selecionadas podem ser apagadas pela acao `Excluir`;
- marcar como lida, acessar o dossie e excluir podem ser feitos individualmente ou em lote, incluindo todas as notificacoes da pagina ou da caixa de entrada.

#### Como essa regra deve orientar um card

- Registrar o usuario, a origem da notificacao, o dossie relacionado, data e horario, estado de leitura, quantidade de itens na listagem, acao executada e resultado apresentado.
- Diferenciar notificacao interna de e-mail, convite de campanha, lembrete e mencao em dossie, sem assumir que uma acao em um canal altera o estado nos demais.
- Validar que a lista inicial mostra as 10 notificacoes mais recentes em ordem cronologica e que `Ver Todas` preserva a listagem completa sem duplicar ou omitir itens.
- Para acoes em lote, testar selecao individual, pagina atual e caixa de entrada completa, garantindo que marcar como lida ou excluir alcance somente os itens selecionados pelo usuario.
- Ao abrir o dossie pelo icone de envelope, validar a correspondencia com a notificacao e aplicar as permissoes do usuario ao dossie de destino; a notificacao nao deve conceder acesso adicional ao conteudo.
- Confirmar com produto e seguranca a definicao de ordem cronologica, limites de retencao, comportamento de exclusao e restauracao, atualizacao entre dispositivos, auditoria, notificacoes nao lidas e regras de permissao para cada origem de evento.

### Lembretes por e-mail

Com base no artigo [Ativar Lembretes por E-mail](https://intercom.help/compliasset/pt-BR/articles/7946246-ativar-lembretes-por-e-mail), publicado em 24 de fevereiro de 2026:

- existem dois tipos de lembrete por e-mail: `Lembrete Semanal` e lembrete personalizado, tambem chamado de diario;
- o Lembrete Semanal e uma notificacao geral relacionada a Agenda, Eventos e Documentos e informa vencimentos proximos, inclusive de demandas que nao pertencem a responsabilidade do destinatario;
- por configuracao padrao, o Lembrete Semanal e destinado a Membros-Administradores e Membros-Usuarios e nao e disponibilizado a usuarios com perfil somente de Colaborador;
- um Membro ativa ou desativa o Lembrete Semanal em `Meu Perfil`, marcando ou desmarcando a opcao e selecionando `Confirmar`;
- o Lembrete Semanal e enviado toda segunda-feira com a listagem de demandas que vencem na semana;
- o lembrete personalizado nao e ativado automaticamente: a empresa deve solicitar sua ativacao ao suporte pelo chat ou e-mail;
- depois de ativado, o lembrete personalizado e enviado apenas aos responsaveis por Atividades, Eventos e Obrigacoes;
- o lembrete diario e enviado de forma regressiva nos sete dias anteriores ao vencimento de Atividades e Eventos;
- o lembrete quinzenal informa Atividades e Eventos ja vencidos que nao tiveram nenhuma acao realizada;
- ao atribuir uma demanda a um Colaborador, ele recebe o lembrete personalizado se a empresa tiver ativado a funcionalidade;
- nao e possivel escolher quais responsaveis receberao o lembrete personalizado: todos os responsaveis pela demanda sao notificados;
- ativar ou desativar o lembrete personalizado nao altera o estado do Lembrete Semanal, e vice-versa.

#### Como essa regra deve orientar um card

- Registrar o tipo de lembrete, empresa, perfil e destinatario, demanda, responsaveis, data de vencimento, horario e periodicidade esperada, estado de ativacao e resultado da entrega.
- Diferenciar Lembrete Semanal e personalizado em escopo, destinatarios, ativacao e periodicidade; nao tratar a mudanca de um como alteracao do outro.
- Para o Lembrete Semanal, validar a restricao padrao a Membros, a configuracao em `Meu Perfil`, o envio na segunda-feira e a inclusao de demandas atribuidas e nao atribuidas que vencem na semana.
- Para o personalizado, validar que a ativacao ocorre no nivel da empresa, que todos os responsaveis sao notificados sem selecao individual e que novos responsaveis passam a receber lembretes somente quando a funcionalidade estiver ativa.
- Testar os lembretes diarios nos sete dias anteriores ao vencimento e os quinzenais para demandas vencidas sem acao, separando Atividades, Eventos, Obrigacoes e Documentos conforme o tipo aplicavel.
- Confirmar com produto, suporte e seguranca os canais e responsaveis pela ativacao, horarios e fusos de envio, definicao de nenhuma acao realizada, tratamento de feriados, limites de destinatarios, regras de reenvio, historico de configuracao e entrega e tratamento de falhas de e-mail.

### Funcoes uteis ativadas internamente

Com base no artigo [6 Funcoes Uteis no Compliasset](https://intercom.help/compliasset/pt-BR/articles/9200338-6-funcoes-uteis-no-compliasset), publicado em 18 de abril de 2024:

- as seis funcoes abaixo sao habilitadas ou desabilitadas internamente pelo time CompliAsset; Membros nao as configuram diretamente no sistema;
- a permissao para Colaboradores alterarem o status permite que eles modifiquem o status de Atividades, Obrigacoes ou Eventos atribuidos a eles;
- a automacao de status altera um dossie de `Em Aberto` para `Em Andamento` quando recebe seu primeiro comentario;
- a criacao de Eventos automaticos gera Eventos de boas praticas quando um novo Relacionado, como um Colaborador, e incluido no sistema;
- os lembretes diarios enviam e-mail a Membros e Colaboradores responsaveis por Atividades e Eventos, de forma regressiva a partir de sete dias antes do vencimento;
- os lembretes de atraso enviam, quinzenalmente, e-mails aos responsaveis por Atividades e Eventos vencidos que nao tiveram nenhuma acao realizada;
- a configuracao de Enquadramento habilita o recebimento de intraday por e-mail apos o fechamento das carteiras.

#### Como essa regra deve orientar um card

- Registrar a empresa ou ambiente, funcao solicitada, estado anterior e desejado, solicitante, aprovador, canal de solicitacao ao suporte e evidencia da ativacao ou desativacao.
- Nao propor controles diretos na interface para essas configuracoes sem uma decisao formal de produto e seguranca; o artigo atribui sua operacao ao time interno do CompliAsset.
- Para permissao de status, validar que o Colaborador altera somente dossies que lhe foram atribuidos e que a transicao preserva historico, responsavel, data e evidencias.
- Para a automacao por comentario, testar o primeiro comentario em dossie `Em Aberto`, impedir nova alteracao automatica nos demais status e preservar o comentario como evidencia que motivou a mudanca.
- Para Eventos automaticos, validar gatilho na inclusao de novo Relacionado, tipos de Evento gerados, ausencia de duplicidade, permissao de desativacao por empresa e trilha de auditoria.
- Aplicar aos lembretes diarios e quinzenais as regras de destinatarios, prazo e ativacao descritas em `Lembretes por e-mail`; esta configuracao nao deve alterar o Lembrete Semanal do perfil.
- Para Enquadramento, registrar carteira, momento de fechamento, destinatarios, conteudo do intraday e resultado da entrega, sem assumir horarios, fontes ou dados enviados sem confirmacao.
- Confirmar com produto, suporte e seguranca a lista vigente de funcoes internas, fluxo de aprovacao, escopo por ambiente, latencia de ativacao, reversao, auditoria, regras de status, definicao de fechamento de carteira e dados do intraday.

### Historico de acessos

Com base no artigo [Historico de Acessos](https://intercom.help/compliasset/pt-BR/articles/4335645-historico-de-acessos), publicado em 26 de janeiro de 2026:

- os Administradores de cada empresa podem visualizar os acessos realizados pelos usuarios no sistema;
- o recurso e acessado em `Configuracoes` > `Auditoria` > `Historico de Acessos`;
- o historico e ordenado do acesso mais recente para o mais antigo;
- cada registro apresenta data e horario, nome do usuario, numero de IP e localizacao com cidade, estado e pais;
- a acao `Exportar`, no inicio da tela, permite exportar as informacoes do historico.

#### Como essa regra deve orientar um card

- Registrar a empresa, perfil que consultou o historico, periodo avaliado, usuario pesquisado quando aplicavel, data e horario do acesso, IP mascarado e localizacao exibida, sem replicar dados pessoais desnecessarios no card.
- Restringir a consulta e a exportacao aos Administradores da empresa e validar o bloqueio para Colaboradores e Membros-Usuarios, inclusive por URL direta, API e sessao ja ativa.
- Validar a ordenacao decrescente por acesso, a consistencia entre os campos exibidos e o registro de origem e a atualizacao de novos acessos no historico.
- Para exportacoes, registrar quem solicitou, o escopo e o arquivo gerado; tratar IP e localizacao como dados pessoais ou de seguranca e aplicar controles de acesso, finalidade, retencao e compartilhamento.
- Nao assumir que a localizacao e precisa ou que um IP identifica uma pessoa; apresentar tais informacoes como dados tecnicos de apoio a investigacao.
- Confirmar com produto, seguranca e privacidade o formato e destino da exportacao, filtros e periodo disponiveis, tempo de retencao, criterios de geolocalizacao, mascaramento de IP, auditoria das consultas e exportacoes e tratamento de acessos por VPN, proxy ou dispositivos compartilhados.

### Navegacoes de usuarios

Com base no artigo [Navegacoes de Usuarios](https://intercom.help/compliasset/pt-BR/articles/16680587-navegacoes-de-usuarios), atualizado na semana de consulta:

- a funcionalidade esta disponivel exclusivamente para usuarios com perfil Administrador e e acessada em `Configuracoes` > `Auditoria` > `Navegacoes de Usuarios`;
- a tela apresenta o historico de utilizacao da plataforma por Colaboradores, incluindo total de navegacoes, usuario, local ou funcionalidade acessada, data e horario;
- os filtros disponiveis sao `Usuario`, com busca por lupa, e `Periodo`; a lista e atualizada pela acao `Filtrar`;
- ao selecionar um Colaborador, a visualizacao detalhada apresenta telas mais acessadas e sua quantidade, volume de acessos e historico recente de navegacao;
- o relatorio individual pode ser exportado ao selecionar o Colaborador e usar `Exportar`, gerando arquivo Excel no formato `.xlsx` com as informacoes exibidas na consulta.

#### Como essa regra deve orientar um card

- Distinguir Navegacoes de Usuarios de Historico de Acessos: o primeiro registra utilizacao de telas e funcionalidades, enquanto o segundo registra eventos de acesso com IP e localizacao.
- Registrar o Administrador que consultou, empresa ou ambiente, Colaborador analisado, filtros de usuario e periodo, quantidade retornada, detalhe consultado, exportacao solicitada e resultado.
- Restringir a consulta, detalhamento e exportacao a Administradores, validando o bloqueio a Membros-Usuarios e Colaboradores por menu, URL direta, API e sessao ativa.
- Validar os filtros individualmente e combinados, a atualizacao pela acao `Filtrar`, a coerencia entre total de navegacoes, telas mais acessadas e historico recente e a ausencia de dados de outro ambiente.
- Para a exportacao individual, conferir que o Excel `.xlsx` corresponde ao Colaborador e aos filtros consultados e aplicar os controles de dados pessoais, finalidade, compartilhamento, retencao e auditoria da exportacao.
- Confirmar com produto, seguranca e privacidade a definicao de Administrador elegivel, retencao, fuso horario, significado de navegacao, granularidade de local, ordenacao do historico recente, disponibilidade dos filtros, destino do arquivo e disponibilidade em `Downloads`.

### Tokens de API

Com base no artigo [API Token](https://intercom.help/compliasset/pt-BR/articles/8141236-api-token), publicado em 19 de julho de 2023:

- a configuracao da API fica em `Configuracoes` > `API Token`;
- a tela disponibiliza a documentacao da API CompliAsset, incluindo Autenticacao, Paginacao e Codigos de Erro;
- a acao `+` permite criar novas chaves de API;
- uma chave criada pode ser excluida pelo botao de lixeira na linha correspondente.

#### Como essa regra deve orientar um card

- Registrar o ambiente, sistema de origem e destino, finalidade da integracao, chave identificada apenas por nome ou identificador seguro, responsavel pela acao e resultado, sem incluir token, segredo, valor de cabecalho ou credencial em cards, logs, anexos ou mensagens.
- Testar separadamente o acesso a documentacao, a criacao e a exclusao da chave, confirmando que cada acao se aplica somente ao ambiente e chave selecionados.
- Para integracoes, consultar e referenciar a documentacao oficial de autenticacao, paginacao e codigos de erro; nao implementar a partir da descricao resumida deste artigo.
- Tratar a exclusao como operacao sensivel: antes de executa-la, identificar dependencias e registrar a decisao; confirmar se a chave deixa de autenticar imediatamente e como falhas de integracao serao tratadas.
- Restringir a gestao de chaves aos perfis autorizados e validar o bloqueio por interface, URL direta e API para perfis sem permissao.
- Confirmar com produto e seguranca os perfis autorizados, escopos, validade, rotacao, limite de chaves, exibicao unica do segredo, revogacao, auditoria, notificacoes, armazenamento seguro e ambientes atendidos.

### Navegacao entre empresas

Com base no artigo [Navegar entre Empresas](https://intercom.help/compliasset/pt-BR/articles/5117898-navegar-entre-empresas), publicado em 6 de dezembro de 2023:

- quando uma empresa possui mais de um ambiente no sistema, o usuario pode navegar entre eles pelo proprio acesso;
- na visao de Membro, a troca ocorre pelo botao com as iniciais ou avatar, no canto superior direito da tela, seguido da selecao do ambiente desejado;
- na visao de Colaborador, a troca ocorre pelo botao com as iniciais ou avatar, no canto superior esquerdo da tela, seguido da selecao do ambiente desejado.

#### Como essa regra deve orientar um card

- Registrar a visao usada, ambiente de origem, ambiente de destino, usuario, momento da troca, seletor utilizado e o resultado apresentado apos a selecao.
- Testar os seletores separadamente na visao de Membro e na visao de Colaborador, pois ocupam posicoes diferentes na interface.
- Para falhas de troca, verificar se o ambiente esperado aparece para o acesso, se os dados e permissoes exibidos pertencem ao destino e se a navegacao preserva somente o contexto compativel com o novo ambiente.
- Nao presumir que todo usuario pode acessar todos os ambientes da empresa, nem que a troca de ambiente equivale a trocar de perfil ou de visao; tratar essas regras como dependencias de permissao separadas.
- Confirmar com produto e seguranca os criterios que definem a lista de ambientes disponiveis, o comportamento de sessao, URLs, notificacoes, dados em cache, auditoria da troca e o tratamento de ambientes inativos ou indisponiveis.

### Alternancia entre visao de Usuario e Colaborador

Com base no artigo [Navegando entre Visao de Usuario e Colaborador](https://intercom.help/compliasset/pt-BR/articles/6032604-navegando-entre-visao-de-usuario-e-colaborador), publicado em 28 de abril de 2025:

- usuarios com acesso de Membro podem alternar entre a visao de Usuario, tambem denominada visao de Membro, e a visao de Colaborador;
- na visao de Usuario, a troca ocorre pelo botao com iniciais ou avatar no canto superior direito, ao lado do icone de notificacoes, selecionando `Visao do Colaborador`;
- na visao de Colaborador, o retorno ocorre pelo seletor `Visao do Colaborador` no canto esquerdo da tela, selecionando `Visao de Usuario`;
- participar de Treinamentos e preencher Formularios sao acoes que devem ser executadas exclusivamente na visao de Colaborador.

#### Como essa regra deve orientar um card

- Registrar o usuario, perfil, visao de origem e destino, ambiente, acao selecionada, contexto de sessao e resultado, distinguindo a alternancia de visao da troca de empresa.
- Validar que apenas usuarios com acesso de Membro podem alternar para a visao de Colaborador e que o retorno para `Visao de Usuario` restaura somente as permissoes do perfil de Membro efetivamente concedidas.
- Testar os caminhos nos dois sentidos e suas posicoes distintas na interface, incluindo recarregamento, nova sessao e troca de ambiente quando aplicavel.
- Para Treinamentos e Formularios, validar que a execucao pelo destinatario ocorre na visao de Colaborador e que a visao de Usuario nao contorna as regras de matricula, campanha, preenchimento ou historico.
- Preservar o contexto do usuario e o isolamento de dados e permissoes ao trocar de visao; a troca nao deve ampliar acesso a registros, dossies ou funcoes nao concedidas.
- Confirmar com produto e seguranca quais perfis de Membro podem alternar, o comportamento em sessoes ativas, URLs, notificacoes, registros de auditoria, estado de formularios ou treinamentos em andamento e as diferencas entre visao de Usuario e de Membro na versao atual.

### Guia de primeiro acesso

Com base no artigo [Guia de Primeiro Acesso](https://intercom.help/compliasset/pt-BR/articles/6695329-guia-de-primeiro-acesso), publicado em 29 de abril de 2026:

- quando um novo cadastro e realizado, o e-mail de boas-vindas com login e senha temporaria e enviado por `contato@compliasset.com`;
- o acesso pode ser iniciado pelo link do e-mail ou diretamente pela tela de login;
- deve-se priorizar o link recebido no e-mail para assegurar o uso do dominio correto da empresa, que pode ser `app`, `abrapp`, `payments` ou outro;
- o primeiro login usa o e-mail cadastrado e a senha temporaria; a tela tambem apresenta as opcoes de acesso por Office 365 e Google;
- caso o e-mail com senha tenha sido perdido ou seja necessario trocar a senha, o usuario acessa `Esqueceu sua senha?`, informa o e-mail cadastrado, seleciona `Recuperar` e usa o link recebido para criar uma nova senha;
- uma pessoa pode informar o e-mail cadastrado de outro colega no fluxo de recuperacao para auxiliá-lo, conforme orientacao do artigo;
- quando houver duvida ou falha no processo, o canal de suporte informado e chat ou `suporte@compliasset.com`.

#### Como essa regra deve orientar um card

- Registrar o tipo de primeiro acesso, o ambiente ou dominio usado, o metodo de login, o estado do cadastro, a etapa que falhou e a mensagem exibida, sem incluir senha temporaria, credenciais ou link de recuperacao.
- Para ausencia do e-mail de boas-vindas, verificar o remetente `contato@compliasset.com`, o endereco cadastrado, spam ou bloqueios de dominio e o resultado do reenvio administrativo antes de concluir que houve falha de cadastro.
- Testar separadamente o acesso pelo link de convite, o login direto pelo dominio correto, Office 365, Google e a recuperacao de senha, pois sao caminhos distintos para chegar ao acesso.
- Preservar a troca de senha temporaria e aplicar os controles de expiracao, uso unico, limite de envio e protecao contra enumeracao de contas aos links de recuperacao.
- Tratar o pedido de recuperacao para o e-mail de um colega como solicitacao que nao pode revelar se a conta existe, seu status ou outros dados pessoais ao solicitante.
- Confirmar com produto e seguranca o remetente vigente, os dominios e metodos disponiveis por ambiente, a obrigatoriedade da troca inicial de senha, o comportamento de Office 365 e Google para novos cadastros e as protecoes contra abuso do fluxo de recuperacao.

### FAQ de acesso e login

Com base no artigo [FAQ - Acesso e Login](https://intercom.help/compliasset/pt-BR/articles/9641358-faq-acesso-e-login), publicado em 5 de março de 2026:

- os links de acesso informados no artigo sao `https://app.compliasset.com/signin` para Empresas, `https://abrapp.compliasset.com/signin` para Previdencia e `https://payments.compliasset.com/signin` para Pagamentos;
- o cadastro deve ser realizado por um membro do time que ja tenha acesso; para o primeiro acesso do super administrador, as credenciais sao enviadas no e-mail `Bem vindo ao Compliasset`;
- os metodos de login informados sao senha propria, Google, Office 365 e SSO;
- diante de `usuario e senha invalidos`, deve-se conferir o e-mail cadastrado, a senha digitada e a tecla `CAPS LOCK`; a tela tambem pode permitir visualizar a senha pelo icone de olho;
- se o problema persistir, o usuario deve usar `Esqueceu sua senha?` e seguir as instrucoes recebidas por e-mail;
- quando o e-mail nao chega, deve-se verificar spam, lixo eletronico, bloqueios ao dominio `@compliasset.com`, cadastro do e-mail e status de bloqueio do acesso;
- o contato com suporte deve incluir, no inicio, um print do erro e o link de acesso utilizado; o canal informado e chat ou `suporte@compliasset.com`;
- o bloqueio por tentativas invalidas notifica o time de compliance da empresa, que deve realizar o desbloqueio, ou o usuario pode aguardar 24 horas;
- o artigo associa o erro 500 a e-mail desativado no sistema ou e-mail vinculado a ambiente deletado;
- diante da mensagem `A empresa que você está tentando conectar não está mais disponível`, a orientacao e acionar o suporte;
- a autenticacao de dois fatores pode ser ativada para exigir um codigo enviado ao e-mail durante o login;
- somente usuarios cadastrados como colaboradores possuem acesso; Terceiros cadastrados nao acessam o sistema.

#### Como essa regra deve orientar um card

- Registrar sempre o ambiente acessado, o link completo, o metodo de autenticacao, o perfil do usuario, a mensagem exibida e se o e-mail esta ativo e vinculado a um ambiente existente.
- Para falhas de login, separar erro de credencial, senha expirada, bloqueio, erro 500, empresa indisponivel e falha de entrega de e-mail.
- Nao colocar credenciais, codigos de segundo fator, links de redefinicao ou dados pessoais desnecessarios em prints, cards e chamados.
- Tratar os links de ambiente e os metodos Google, Office 365 e SSO como configuracao que deve ser confirmada antes de alterar telas ou documentacao.
- Ha uma divergencia a confirmar com produto e seguranca sobre o desbloqueio: este FAQ atribui a acao ao time de compliance, enquanto os artigos anteriores descrevem Administrador e desbloqueio automatico apos 24 horas.
- Confirmar tambem o comportamento esperado para e-mails desativados, ambientes deletados, empresas indisponiveis, usuarios Terceiros e solicitacoes de suporte.

### FAQ de cadastros de colaboradores

Com base no artigo [FAQ - Cadastros de Colaboradores](https://intercom.help/compliasset/pt-BR/articles/9653170-faq-cadastros-de-colaboradores), publicado em 29 de julho de 2024:

- um colaborador pode ser cadastrado manualmente, por importacao de planilha em massa ou via API;
- nome e e-mail sao obrigatorios no cadastro; os demais dados podem ser adicionados depois;
- o sistema nao permite reutilizar o e-mail de um colaborador desativado ou excluido, por causa do historico relacionado ao usuario; a recomendacao e usar um novo e-mail;
- o acesso de um colaborador e desativado pela inclusao de uma data de desligamento em seu perfil;
- a importacao de planilha permite cadastrar varios colaboradores e tambem atualizar varios perfis simultaneamente;
- na importacao, o e-mail e o identificador: um e-mail novo cria cadastro e um e-mail ja existente atualiza o perfil conforme a planilha;
- o cadastro pode criar eventos automaticamente com recomendacoes e boas praticas; a desativacao desse comportamento depende de contato com o suporte;
- se o e-mail de boas-vindas nao for recebido, e possivel usar `Reenviar` no perfil ou solicitar redefinicao pela tela de login;
- um colaborador recem-cadastrado aparece inicialmente em `Bloqueados` e passa para `Time Atual` depois do primeiro login e da troca da senha.

#### Como essa regra deve orientar um card

- Identificar a origem do cadastro ou atualizacao, o e-mail usado como identificador, o perfil afetado e se a operacao e inclusao, atualizacao ou desativacao.
- Para importacoes, preservar o arquivo de entrada, o resultado por linha, as regras de duplicidade e o tratamento de e-mails novos, existentes, desativados ou excluidos, sem incluir dados pessoais desnecessarios.
- Nao propor a reutilizacao de e-mail historico sem revisar identidade, rastreabilidade, isolamento entre empresas e impacto em eventos e acessos anteriores.
- Ao alterar o cadastro, considerar e-mail de boas-vindas, senha temporaria, bloqueio inicial, data de desligamento e eventos automaticos desencadeados.
- Tratar cadastro manual, importacao e API como fluxos distintos, com permissoes, validacoes, limites, erros parciais e auditoria proprios.
- Confirmar com produto e tecnologia os campos aceitos pela planilha e API, a regra de atualizacao por e-mail, os eventos automaticos criados e o tratamento de registros desativados ou excluidos.

### Upload de novos colaboradores

Com base no artigo [Upload de Novos Colaboradores](https://intercom.help/compliasset/pt-BR/articles/5520614-upload-de-novos-colaboradores), publicado em 26 de abril de 2024:

- o cadastro de Colaboradores pode ser manual ou feito em lote por planilha, e o mesmo fluxo tambem permite atualizar informacoes de colaboradores existentes;
- para importar ou atualizar, o usuario acessa `Colaboradores` > `Todos os Colaboradores` > `+` > `Importar`;
- a tela de importacao disponibiliza o arquivo modelo, que deve ser baixado e seguido na ordem e estrutura indicadas;
- a primeira linha do modelo deve ser mantida e os dados devem ser preenchidos a partir da segunda linha, com os campos separados por virgulas;
- depois de preencher o arquivo, o usuario seleciona a planilha e clica em `Importar`; antes da confirmacao, o sistema exibe os dados que serao refletidos no cadastro;
- a pre-visualizacao apresenta um indicador colorido ao lado de cada Colaborador para sinalizar reativacao, primeiro cadastro ou atualizacao;
- a confirmacao final ocorre pelo botao `Criar/Atualizar Colaboradores`;
- no campo de envio do e-mail de boas-vindas, o valor `1` solicita o envio e o valor `0` impede o envio;
- o e-mail de boas-vindas via planilha so pode ser enviado uma vez e esse campo nao pode ser atualizado posteriormente;
- campos opcionais podem ser deixados em branco ou representados por duas virgulas consecutivas (`,,`); quando a planilha for montada em colunas, a celula pode permanecer vazia;
- para atualizar um Colaborador por upload, o e-mail informado deve ser o mesmo que ja esta cadastrado no sistema;
- o limite informado para a planilha e de ate 100 Colaboradores por importacao;
- o arquivo preparado no Excel ou no Google Sheets deve ser exportado como `.csv` com os elementos separados por virgulas.

#### Como essa regra deve orientar um card

- Diferenciar cadastro manual, importacao de novos Colaboradores, reativacao e atualizacao de cadastro, registrando o estado indicado na pre-visualizacao.
- Validar o caminho para baixar o modelo, preservar a primeira linha, respeitar a ordem das colunas, usar virgulas como delimitador e limitar o arquivo a 100 Colaboradores.
- Testar os indicadores de primeiro cadastro, atualizacao e reativacao e conferir que a confirmacao por `Criar/Atualizar Colaboradores` persiste exatamente os dados exibidos na pre-visualizacao.
- Testar os valores `1` e `0` do e-mail de boas-vindas, a regra de envio unico e a impossibilidade de atualizar esse campo em uma importacao posterior, sem registrar credenciais ou links reais.
- Para atualizacoes, validar a correspondencia pelo e-mail existente, o tratamento de e-mail novo ou divergente, a ausencia de duplicidade e a preservacao dos demais dados do Colaborador.
- Confirmar com produto e tecnologia o significado exato das cores e estados, os campos do modelo, a regra para reativacao, o tratamento de erros ou processamento parcial, a permissao para importar e atualizar e a auditoria das alteracoes.

### Atualizacao de Colaboradores por Upload de Planilha

Com base no artigo [Atualizacao de Colaboradores](https://intercom.help/compliasset/pt-BR/articles/15001248-atualizacao-de-colaboradores), publicado em 7 de maio de 2026:

- a atualizacao em massa e iniciada em `Colaboradores` > `Todos os Colaboradores`, pela acao `+`;
- o sistema disponibiliza um modelo de planilha em `Baixe o arquivo modelo de importacao`, acompanhado de instrucoes;
- `Nome` e `E-mail` devem ser informados como campos obrigatorios de identificacao para que os dados sejam atualizados;
- Nome e E-mail nao devem ser alterados pela planilha; solicitacoes para altera-los devem ser encaminhadas a equipe tecnica pelo e-mail `suporte@compliasset.com`;
- os demais campos podem ser atualizados, incluindo `Ramal`, `Celular`, `CEP`, `Endereco`, `Numero`, `Complemento`, `Cidade`, `Estado`, `Pais`, `CPF`, `RG`, `Profissao`, `Departamento`, `Cargo`, `Data de Contratacao` e `Data de Demissao`;
- a coluna de envio de e-mail de boas-vindas deve permanecer com o valor `0`, embora seu preenchimento seja obrigatorio;
- a primeira linha do modelo nao deve ser apagada e nenhuma coluna deve ser excluida; campos sem preenchimento devem permanecer vazios;
- e-mails apagados podem reativar os cadastros correspondentes, conforme a regra descrita no artigo;
- cada importacao aceita no maximo 100 Colaboradores e o arquivo deve possuir extensao `.csv`;
- o e-mail de boas-vindas nao e enviado para Colaboradores atualizados, pois esse envio ocorre somente na criacao de um novo Colaborador;
- durante a importacao, o sistema identifica os registros em atualizacao; ao final, o usuario seleciona `Importar` para confirmar a operacao.

#### Como essa regra deve orientar um card

- Registrar Colaboradores, campos alterados, Nome e E-mail usados como identificadores, usuario executor, arquivo, quantidade de linhas, estado exibido durante a importacao e resultado final, sem expor dados pessoais desnecessarios.
- Validar o caminho `Colaboradores` > `Todos os Colaboradores` > `+`, o download do modelo, a preservacao da primeira linha, a ordem das colunas e a extensao `.csv`.
- Testar a atualizacao de cada campo permitido e confirmar que Nome e E-mail nao podem ser alterados pelo upload, direcionando essas solicitacoes ao fluxo tecnico de suporte.
- Validar o valor `0` na coluna de boas-vindas, sua obrigatoriedade, a ausencia de envio para atualizacoes e o envio somente no cadastro de um novo Colaborador.
- Testar ate 100 registros, arquivo acima do limite, campos vazios, colunas removidas, formato invalido, e-mail inexistente, e-mail apagado e processamento parcial ou bloqueado.
- Conferir que os dados apresentados ou identificados como em atualizacao correspondem aos dados efetivamente persistidos somente apos a confirmacao por `Importar`.
- Diferenciar atualizacao cadastral, reativacao por e-mail e criacao de novo Colaborador; nenhum desses fluxos deve apagar responsabilidades, historico ou evidencias sem regra especifica.
- Confirmar com produto, tecnologia e suporte os campos aceitos, a semantica de e-mails apagados, o comportamento de erros e duplicidades, o processamento parcial ou rollback, as permissoes, a auditoria e os efeitos sobre acesso, notificacoes e responsabilidades.

### Upload de Relacionados via Planilha

Com base no artigo [Upload de Relacionados via Planilha](https://intercom.help/compliasset/pt-BR/articles/4570873-upload-de-relacionados-via-planilha), publicado em 15 de agosto de 2023:

- o upload de planilhas permite carregar multiplos cadastros de Relacionados sem inclusao manual registro a registro;
- o artigo orienta o upload de `Fundos`, `Investidores` e `Terceiros`, alem de indicar uma secao propria para `Colaboradores`;
- cada area possui um modelo de planilha diferente, que deve ser preenchido conforme as instrucoes da respectiva secao;
- as regras de campos, identificadores, formatos, limites, atualizacao e tratamento de erros devem ser consultadas no artigo especifico de cada tipo de Relacionado;
- o suporte indicado para duvidas sobre o upload e o chat ou o e-mail `suporte@compliasset.com`.

#### Como essa regra deve orientar um card

- Classificar o cadastro como Fundo, Investidor, Terceiro ou Colaborador antes de definir o modelo, os campos e o fluxo de importacao.
- Registrar empresa ou ambiente, tipo de Relacionado, usuario executor, modelo utilizado, quantidade de registros, resultado da validacao, registros criados ou atualizados e erros por linha, minimizando dados pessoais nas evidencias.
- Nao reutilizar o modelo de uma area em outra nem inferir campos obrigatorios, identificadores ou limites a partir deste artigo geral; consultar a fonte especifica do cadastro.
- Validar a preservacao da estrutura do modelo, a extensao e o delimitador aceitos, campos vazios, duplicidades, pre-visualizacao, confirmacao, processamento parcial ou rollback conforme a regra do tipo de Relacionado.
- Diferenciar carga inicial, atualizacao de cadastros existentes e reativacao; cada operacao deve explicitar sua chave de identificacao, permissao, auditoria e efeito nos vinculos com Eventos, Grupos e demais dossies.
- Confirmar com produto e tecnologia os caminhos de acesso, modelos vigentes, campos obrigatorios, identificadores, limites, codificacao, mensagens de erro, permissao de importacao e retencao dos arquivos enviados.

### Upload de Novos Investidores

Com base no artigo [Upload de Novos Investidores](https://intercom.help/compliasset/pt-BR/articles/7919004-upload-de-novos-investidores), publicado em 5 de julho de 2023:

- o upload e iniciado em `Investidores` > `Todos os Investidores` > `+` > `Importar uma Lista de Investidores`;
- o sistema disponibiliza um modelo de importacao com as colunas `Nome Completo/Razao Social`, `Nome fantasia`, `Tipo de Pessoa`, `E-mail`, `CPF/CNPJ`, `Data de entrada`, `Data de Saida` e `Risco`;
- `Nome Completo/Razao Social`, `Tipo de Pessoa`, `E-mail` e `CPF/CNPJ` sao obrigatorios; nomes e e-mails aceitam ate 255 caracteres;
- os codigos documentados sao `1` para Pessoa Juridica, `2` para Pessoa Fisica e `3` para Estrangeiro, e `1`, `2`, `3` e `0` para risco baixo, medio, alto e `N/A`;
- as datas devem usar o formato `dd/mm/yyyy`; campos vazios devem preservar a separacao por virgulas consecutivas (`,,`);
- a primeira linha do modelo deve ser mantida e os dados devem comecar na segunda linha;
- o arquivo precisa ser `.csv`, com elementos separados por virgulas;
- depois de `Importar`, o sistema exibe uma simulacao para conferencia e a confirmacao ocorre por `Criar/Atualizar Investidores`.

#### Como essa regra deve orientar um card

- Registrar modelo, Investidor, usuario executor, quantidade de linhas, simulacao, registros criados ou atualizados, erros por linha e resultado final, minimizando CPF, CNPJ e e-mails nas evidencias.
- Validar o caminho de importacao, a preservacao da primeira linha, a ordem das colunas, a extensao `.csv`, o delimitador, os campos obrigatorios, limites de caracteres, codigos de pessoa e risco e formato de datas.
- Testar campos opcionais vazios, acentos e codificacao do arquivo, duplicidades, e-mail ou CPF/CNPJ invalidos e a correspondencia entre simulacao e dados persistidos.
- Diferenciar simulacao de confirmacao: nenhum registro deve ser criado ou atualizado antes de `Criar/Atualizar Investidores`, salvo regra atual confirmada em contrario.
- Confirmar com produto e tecnologia a chave de identificacao de registros existentes, semantica de `Atualizar`, limite de linhas, processamento parcial ou rollback, permissao, auditoria e efeitos sobre Eventos e Grupos.

### Upload de novos participantes

Com base no artigo [Upload de Novos Participantes](https://intercom.help/compliasset/pt-BR/articles/8095579-upload-de-novos-participantes), publicado em 5 de julho de 2023:

- a importacao em massa e iniciada em `Participantes` > `Todos os Participantes`, pela acao `+` > `Importar uma Lista de Participantes`;
- o sistema disponibiliza um modelo padrao de planilha para a importacao; a primeira linha, que contem os nomes e orientacoes das colunas, nao deve ser removida;
- os dados devem ser preenchidos a partir da segunda linha e exportados como arquivo `.csv` com os elementos separados por virgulas;
- as colunas do modelo sao `Nome Completo/Razao Social`, `Nome fantasia`, `Tipo de Pessoa`, `E-mail`, `CPF/CNPJ`, `Data de entrada`, `Data de Saida` e `Risco`;
- `Nome Completo/Razao Social`, `Tipo de Pessoa`, `E-mail` e `CPF/CNPJ` sao obrigatorios; o nome e a razao social aceitam ate 255 caracteres e o e-mail aceita ate 255 caracteres;
- os valores documentados para `Tipo de Pessoa` sao `1` para Pessoa Juridica, `2` para Pessoa Fisica e `3` para Estrangeiro;
- os valores documentados para `Risco` sao `1` para baixo, `2` para medio, `3` para alto e `0` para `N/A`;
- as datas devem seguir o formato `dd/mm/yyyy`; para deixar um campo vazio, a linha deve manter a separacao das colunas usando duas virgulas consecutivas;
- depois de selecionar o `.csv`, o sistema apresenta uma simulacao dos dados carregados para conferencia;
- a confirmacao ocorre pela acao `Criar/Atualizar Participantes`; o artigo nao detalha quais campos identificam um participante existente nem em que situacoes a operacao atualiza ou cria um cadastro;
- o artigo orienta procurar o chat ou `suporte@compliasset.com` em caso de duvida.

#### Como essa regra deve orientar um card

- Diferenciar a importacao geral em `Todos os Participantes` da importacao de participantes em `Grupos`; os fluxos possuem telas, modelos e objetivos diferentes.
- Registrar empresa ou ambiente, usuario responsavel, arquivo de origem, quantidade de linhas, resultado da simulacao, registros criados ou atualizados e erros por linha, sem expor CPF, CNPJ, e-mail ou outros dados pessoais desnecessarios.
- Validar a preservacao da primeira linha do modelo, a leitura por virgulas, a extensao `.csv`, as colunas na ordem esperada, os campos obrigatorios, os limites de caracteres, o formato de data e os codigos de tipo de pessoa e risco.
- Testar campos opcionais vazios sem deslocar os valores das colunas seguintes e conferir a correspondencia entre a simulacao e os dados efetivamente persistidos.
- Diferenciar a simulacao da confirmacao: nenhum participante deve ser criado ou atualizado antes de `Criar/Atualizar Participantes`, salvo regra atual confirmada em sentido contrario.
- Confirmar com produto e tecnologia a permissao para importar, a chave de identificacao de registros existentes, a semantica de `Atualizar`, tratamento de duplicidades, rollback ou processamento parcial, limite de linhas, codificacao do arquivo, mensagens de erro, auditoria e efeitos em participantes ja vinculados a Eventos ou outros modulos.

### Regras gerais para upload de planilhas

Com base no artigo [Regras e Orientacao para Upload de Planilhas](https://intercom.help/compliasset/pt-BR/articles/11830342-regras-e-orientacao-para-upload-de-planilhas), publicado em 25 de julho de 2025:

- as importacoes descritas devem usar arquivo `.CSV`, inclusive quando a planilha tiver sido preparada no Excel ou no Google Sheets;
- a primeira coluna do modelo nao deve ser apagada nem reestruturada;
- campos obrigatorios devem ser preenchidos; campos opcionais podem ficar em branco ou ser representados por duas virgulas consecutivas (`,,`);
- depois de preparar o arquivo, o usuario deve carrega-lo na area de importacao e selecionar `Importar`;
- antes da confirmacao, o sistema exibe os dados da planilha e destaca informacoes fora do padrao; enquanto houver erro, a importacao nao pode ser concluida e o botao permanece desabilitado;
- a importacao de Colaboradores aceita no maximo 100 registros por vez; exige `Nome` e `E-mail` e envia o e-mail de boas-vindas somente para novos usuarios;
- a planilha de Colaboradores pode atualizar cadastros existentes, mas `Nome` e `E-mail` nao podem ser alterados por esse fluxo; o e-mail identifica novos cadastros e atualizacoes e evita duplicidades;
- ao adicionar uma data de contratacao e remover a data de demissao de um Colaborador ja cadastrado, o sistema reativa automaticamente o perfil, alterando o status de desligado para usuario ativo;
- a importacao de Fundos exige `Nome` e `CPF/CNPJ` e aceita no maximo 1000 registros por vez; o sistema usa o CNPJ para identificar novos cadastros e atualizacoes;
- a importacao de Investidores exige `Nome` e `CPF/CNPJ`; o artigo informa o limite de 1000 registros por vez, embora descreva esse limite como `fundos`, ponto que precisa ser confirmado;
- a importacao de Terceiros exige `Razao Social/Nome Completo`, `CPF/CNPJ/Passaporte/RNE`, `CEP`, `Endereco`, `Numero`, `Estado`, `Cidade` e `Pais`, e aceita no maximo 1000 registros por vez;
- para Terceiros, o sistema identifica novos cadastros e atualizacoes pelos documentos `CPF/CNPJ`; o artigo nao esclarece a identificacao quando o participante usa Passaporte ou RNE;
- para Fundos, Investidores e Terceiros, os campos obrigatorios ausentes interrompem a importacao, e os registros sao identificados para evitar duplicidades.

#### Como essa regra deve orientar um card

- Separar as regras transversais de arquivo e validacao das regras especificas de Colaboradores, Fundos, Investidores e Terceiros, sem assumir que o mesmo identificador ou limite vale para todos.
- Registrar tipo de cadastro, empresa ou ambiente, usuario responsavel, arquivo, quantidade de linhas, resultado da pre-validacao, erros destacados, registros criados ou atualizados e status final, minimizando dados pessoais nas evidencias.
- Validar que a primeira coluna permanece intacta, que o arquivo esta em `.CSV`, que campos opcionais vazios nao deslocam colunas e que o botao de importacao fica bloqueado enquanto houver erro de formato ou campo obrigatorio.
- Para Colaboradores, testar limite de 100 registros, envio de boas-vindas somente para novos cadastros, impossibilidade de alterar Nome e E-mail e reativacao ao informar contratacao e remover desligamento.
- Para Fundos, Investidores e Terceiros, testar limite de 1000 registros, identificacao de existentes, ausencia de duplicidade e interrupcao por campos obrigatorios ausentes.
- Nao transformar em criterio de aceite o limite descrito como `1000 fundos` para Investidores sem confirmar se se trata de erro editorial ou regra do produto.
- Confirmar com produto e tecnologia a codificacao e delimitador aceitos, o limite real por modulo, os identificadores de atualizacao, o tratamento de CPF/CNPJ/Passaporte/RNE, processamento parcial ou rollback, auditoria, mensagens de erro e efeitos da reativacao sobre acesso, historico e notificacoes.

### Grupos, departamentos e funcoes

Com base no artigo [Grupos, Departamentos e Funcoes](https://intercom.help/compliasset/pt-BR/articles/6808185-grupos-departamentos-e-funcoes), publicado em 20 de junho de 2024:

- `Funcoes` categorizam os perfis dos Colaboradores, como socios, terceirizados, funcionarios, trabalhadores part time ou full time e consultores externos;
- em `Funcoes`, e possivel criar, editar, adicionar Colaboradores, excluir e expandir uma funcao para consultar os Colaboradores associados;
- `Grupos` organizam Colaboradores e outros cadastros para facilitar a selecao em massa ao criar um novo Evento;
- os exemplos de Grupos incluem equipes ou comites de Colaboradores, Fundos de uma familia e Investidores de determinado perfil;
- em `Configuracoes` > `Grupos`, a acao `+` cria um grupo apos definir seu nome e selecionar `Confirmar`; o novo grupo passa a aparecer na listagem;
- em `Grupos`, e possivel editar o titulo, excluir, adicionar participantes manualmente, importar participantes por planilha e expandir um grupo para consultar seus participantes;
- a lista de participantes permite excluir individualmente um integrante;
- a importacao de participantes usa arquivo CSV baseado no modelo disponibilizado pelo sistema; nenhuma coluna do modelo deve ser excluida, mesmo que permaneça sem preenchimento;
- para importacao de Colaboradores, o identificador e o e-mail, o limite e de 100 Colaboradores por arquivo e e-mails ja cadastrados nao atualizam os dados do Colaborador;
- o modelo apresenta os Colaboradores cadastrados; o valor `1` remove o Colaborador do grupo e o valor `0` o inclui no grupo;
- na listagem de participantes, o campo `Tipo` identifica se o integrante e Colaborador, Fundo, Investidor ou Terceiro; para Colaboradores, `Nome`, `Termino de Mandato` e `Cargo` sao dados informados em seu cadastro.
- `Departamentos` sao definidos no cadastro de um novo Colaborador e permitem filtrar os registros relacionados em `Todos os Colaboradores`;
- em `Departamentos`, e possivel criar, editar o nome e excluir um departamento.

#### Como essa regra deve orientar um card

- Diferenciar Funcao, Grupo e Departamento no escopo e na regra de negocio: Funcao categoriza Colaboradores, Grupo apoia a selecao em massa em Eventos e Departamento serve como atributo e filtro de Colaboradores.
- Registrar o tipo de classificacao, o cadastro afetado, titulo ou nome anterior e novo, integrantes associados, acao executada, usuario responsavel e resultado da operacao.
- Para Grupos, validar a selecao em massa ao criar Eventos e conferir que os destinatarios ou registros selecionados correspondem ao grupo escolhido, preservando a evidencia da composicao usada no momento do envio.
- Para importacao de participantes em Grupos, validar o modelo integral, extensao CSV, identificador por e-mail, limite de 100 Colaboradores, tratamento de e-mails ja cadastrados e os comandos `0` para incluir e `1` para remover.
- Distinguir importacao de participantes de atualizacao cadastral: conforme o artigo, e-mails ja cadastrados nao atualizam dados do Colaborador durante esse fluxo.
- Testar inclusao e exclusao manual de participantes, expansao da lista e exibicao de `Tipo`, incluindo Colaborador, Fundo, Investidor e Terceiro quando estiverem disponiveis no grupo.
- Para Departamentos, testar a atribuicao no cadastro do Colaborador e o filtro em `Todos os Colaboradores`, incluindo registros sem departamento e alteracoes posteriores.
- Para Funcoes e Grupos, testar criacao, edicao, adicao de Colaboradores, expansao da lista e exclusao, sem presumir que a exclusao remove, altera ou bloqueia os Colaboradores associados.
- Confirmar com produto as permissoes para gerir cada classificacao, os tipos de cadastro aceitos em Grupos, regras de duplicidade de nomes, codificacao e colunas obrigatorias do CSV, impactos da exclusao, historico de associacoes e efeito de alteracoes de grupo sobre Eventos ja criados ou enviados.

### Definicao dos perfis de acesso

Com base no artigo [Definicao dos Perfis de Acessos](https://intercom.help/compliasset/pt-BR/articles/1956039-definicao-dos-perfis-de-acessos), publicado em 8 de agosto de 2025:

- o sistema possui quatro perfis: Super Administrador, Membro-Administrador, Membro-Usuario e Colaborador; todos os usuarios tambem possuem o perfil de Colaborador;
- o Super Administrador e o principal ponto de contato entre a empresa e o CompliAsset, tem acesso a todas as funcionalidades, recebe todas as comunicacoes e e identificado pela tag verde `Admin` em `Membros`;
- apenas um Super Administrador e permitido por empresa; nenhum outro Membro pode modifica-lo ou exclui-lo, e sua alteracao depende do time CompliAsset, mediante solicitacao a `suporte@compliasset.com`;
- o Super Administrador e responsavel por cadastrar e gerenciar o acesso de Colaboradores e do time de compliance, configurar as funcionalidades iniciais da plataforma e acompanhar se o sistema atende as necessidades da empresa;
- todas as mensagens e notificacoes importantes, incluindo novidades da plataforma, Boletins Diarios e mudancas na Agenda, sao direcionadas a esse perfil;
- para duvidas contratuais, modulos, valores, treinamentos e demais servicos, o artigo indica `comercial@compliasset.com`; para conteudo regulatorio, mapeamento, Alertas e Boletins Diarios, indica `conteudo@compliasset.com`; para usabilidade, indica chat ou `suporte@compliasset.com`;
- o Membro-Administrador acessa todas as secoes, inclusive `Configuracoes`, e pode gerenciar e personalizar o sistema; o artigo cita, entre outras acoes, gestao de Membros, consultas reputacionais, configuracao de canais de Denuncia e Compliance, exclusao de acessos e eventos e criacao de campanhas;
- podem existir varios Membros-Administradores; eles podem editar perfis com acesso apenas de Colaborador e, para outros Membros, o artigo limita a edicao a informacoes basicas, como cargo, departamento, dados de desligamento e alteracao de perfil, respeitada a protecao do Super Administrador;
- o Membro-Usuario possui acesso mais restrito, nao configura funcoes do sistema e pode visualizar e acessar somente as telas definidas por um Membro-Administrador;
- Membros integram o time de compliance e atuam no monitoramento de normas, atribuicao de responsabilidades, acompanhamento de assinaturas de documentos e envio de Treinamentos, Formularios e demais demandas de compliance; nao ha limite documentado para a quantidade de Membros cadastrados;
- Membros-Usuarios apoiam a operacao diaria, inclusive em Atividades, Eventos e cadastros de Colaboradores, dentro das permissoes efetivamente concedidas; a matriz detalhada deste guia prevalece para definir cada acao permitida;
- Membros-Administradores acumulam as funcoes dos Membros-Usuarios e administram configuracoes gerais, perfis e acessos; eles tambem podem receber comunicacoes do sistema, como Boletins Diarios e Alertas Regulatorios;
- o Colaborador nao integra necessariamente o time de Compliance e interage apenas com demandas concedidas, como dossies de Eventos e Aceites de Documentos; tambem pode criar Eventos para reportar situacoes, como presentes ou solicitacoes de investimento pessoal, e contribuir com evidencias em atividades da Agenda que lhe foram atribuidas.

#### Como essa regra deve orientar um card

- Registrar o perfil atual e pretendido, a empresa, o usuario afetado, o responsavel pela solicitacao, as secoes e acoes envolvidas e o motivo operacional da concessao, reducao ou troca de acesso.
- Tratar a existencia de um unico Super Administrador por empresa como invariante: uma troca deve preservar a unicidade e deve ser encaminhada ao time CompliAsset, sem permitir edicao ou exclusao por outro Membro.
- Diferenciar permissao de contato institucional, acesso a secoes, capacidade de executar acoes e perfil base de Colaborador; nao usar o fato de todo usuario ser Colaborador para conceder funcionalidades de Membro.
- Para alteracoes realizadas por Membro-Administrador, separar a edicao de Colaboradores da edicao de outros Membros e bloquear qualquer tentativa de alterar ou excluir o Super Administrador.
- Para demandas de onboarding e administracao, registrar a responsabilidade do Super Administrador sobre acessos e configuracoes iniciais, sem transferir-lhe automaticamente a execucao de todas as tarefas operacionais do sistema.
- Direcionar demandas comercial, de conteudo regulatorio e de usabilidade aos canais documentados, sem incluir dados pessoais, credenciais, tokens ou informacoes contratuais sensiveis alem do necessario.
- Para Membro-Usuario, aplicar em conjunto as regras de visibilidade ampla por secao e a matriz de acoes de `Permissoes de acesso: usuario e administrador`; a descricao geral de apoio a Atividades e Eventos nao substitui a matriz de criar, editar, excluir e arquivar.
- Para Membro-Administrador, validar a gestao de configuracoes, perfis e acessos; para Colaborador, testar somente os dossies, Aceites, Eventos e atividades efetivamente concedidos.
- Confirmar com produto e seguranca a definicao de todas as comunicacoes recebidas pelo Super Administrador, a tag `Admin`, o fluxo de troca conduzido pelo suporte, o alcance das edicoes basicas de outros Membros, as acoes de consultas reputacionais e canais, as responsabilidades de configuracao inicial e as permissoes atuais de cada perfil.

### Cadastro de membros

Com base no artigo [Cadastro de Membros](https://intercom.help/compliasset/pt-BR/articles/1948899-cadastro-de-membros), publicado em 18 de abril de 2024:

- um usuario deve ser cadastrado primeiro como Colaborador antes de receber um perfil de Membro;
- o cadastro de Membro e feito em `Configuracoes` > `Membros`, pela acao `+`;
- no cadastro, deve-se selecionar um Colaborador listado, definir o perfil como Administrador ou Usuario e especificar as areas do sistema as quais ele tera acesso;
- a acao `Confirmar` salva inclusoes, edicoes e alteracoes de perfil;
- para reverter o acesso de Membro para Colaborador, deve-se seguir o mesmo fluxo, selecionar `Colaborador` no campo `Perfil` e confirmar.

#### Como essa regra deve orientar um card

- Registrar o colaborador afetado, o estado e perfil anteriores e novos, as areas liberadas ou removidas, o responsavel pela alteracao, o ambiente e o resultado da confirmacao.
- Tratar como pre-condicao a existencia de cadastro de Colaborador; uma demanda de concessao de acesso nao deve criar Membro sem identidade, vinculo e dados de colaborador validos.
- Testar separadamente inclusao, edicao de perfil, alteracao das areas de acesso e reversao para Colaborador, verificando o acesso efetivo antes e depois de cada mudanca.
- Preservar historico e auditoria de concessoes, reducoes e reversoes de acesso, inclusive para investigar permissoes herdadas ou ainda ativas apos a mudanca de perfil.
- Nao inferir que Administrador e Usuario possuem o mesmo conjunto de permissoes ou que todas as areas podem ser liberadas para qualquer perfil; usar as definicoes de acesso vigentes como fonte complementar.
- Confirmar com produto e seguranca quem pode cadastrar, editar ou reverter Membros, quais areas podem ser atribuidas por perfil, o efeito sobre sessoes ativas, notificacoes, tarefas e responsabilidades existentes e a retencao do historico de acesso.

### Remocao de acesso de membro

Com base no artigo [Remover Acesso de Membro](https://intercom.help/compliasset/pt-BR/articles/9619968-remover-acesso-de-membro), publicado em 19 de julho de 2024:

- somente um Membro-Administrador pode desativar o acesso de outro Membro; Membros-Usuarios e usuarios com perfil apenas de Colaborador nao possuem essa permissao;
- o Super Administrador nao pode ser alterado ou substituido por outro Membro; essa solicitacao deve ser feita ao time CompliAsset por `suporte@compliasset.com`;
- o desligamento e realizado em `Configuracoes` > `Membros`, selecionando `Editar` no cadastro e informando a `Data de Demissao`, seguida de `Confirmar`;
- apos a confirmacao, o Membro perde o acesso e passa a constar na listagem `Desligados`, com seu historico preservado;
- o cadastro correspondente em `Colaboradores` e atualizado automaticamente para o status `Ex-colaborador`, assegurando a perda completa do acesso;
- quando a intencao for manter o vinculo e somente remover as permissoes de Membro, deve-se alterar o perfil para Colaborador, e nao informar uma data de desligamento.

#### Como essa regra deve orientar um card

- Registrar o Membro afetado, perfil, Data de Demissao, Membro-Administrador responsavel, data e hora da confirmacao, estado anterior e posterior em `Membros` e `Colaboradores` e a preservacao do historico.
- Distinguir desligamento de reversao de perfil: desligamento remove o acesso e atualiza o cadastro para `Ex-colaborador`; reversao mantem o vinculo e o perfil de Colaborador.
- Validar que somente Membro-Administrador executa a acao e que o Super Administrador permanece protegido por interface, URL direta, API e sessao ativa.
- Apos o desligamento, testar bloqueio de login, sessoes ativas, acesso aos dossies, notificacoes, downloads, integracoes e a exibicao nas listagens `Desligados` e `Ex-colaborador`.
- Preservar dossies, evidencias, responsabilidades, comentarios e trilha de auditoria do Membro desligado; transferencias ou redistribuicoes de responsabilidades devem seguir regra formal, sem apagar o historico.
- Confirmar com produto e seguranca o momento efetivo do bloqueio, o comportamento para data futura ou retroativa, sessoes existentes, recuperacao ou recontratacao, notificacoes, redistribuicao de tarefas e retencao de dados e auditoria.

### Alteracao de perfis de acesso

Com base no artigo [Alterar Perfis de Acesso](https://intercom.help/compliasset/pt-BR/articles/4680531-alterar-perfis-de-acesso), publicado em 22 de dezembro de 2023:

- para editar um Membro, deve-se acessar `Configuracoes` > `Membros`, localizar o cadastro na listagem e selecionar `Editar`, identificado pelo icone de lapis;
- no campo `Perfil`, e possivel alterar o cadastro entre Administrador, Usuario e Colaborador;
- o atalho `Fazer Usuario` altera um Administrador para Usuario, e o atalho `Fazer Admin` altera um Usuario para Administrador;
- para ajustar as secoes disponiveis, deve-se selecionar as areas desejadas em `Acessos` e clicar em `Confirmar` ao final da tela;
- a alteracao de perfil pode reduzir secoes que o Membro nao utiliza ou ampliar seu acesso ao menu central;
- as restricoes e diferencas entre os perfis devem seguir a definicao de perfis, a regra de acesso por secao e a matriz de permissoes deste guia.

#### Como essa regra deve orientar um card

- Registrar o caminho usado, o perfil anterior e novo, as secoes antes e depois, o atalho ou campo utilizado, o responsavel, o momento da confirmacao e o resultado efetivo do acesso.
- Testar separadamente as transicoes Administrador para Usuario, Usuario para Administrador e Membro para Colaborador, conferindo que as telas, dados e acoes do perfil anterior deixam de estar disponiveis quando aplicavel.
- Validar que `Fazer Usuario` e `Fazer Admin` produzem a mesma alteracao de perfil esperada pelo campo `Perfil`, sem ignorar as regras de acesso por secao ou conceder permissoes adicionais.
- Para alteracoes em `Acessos`, validar que somente `Confirmar` persiste a selecao e que a visibilidade ampla por secao do Membro-Usuario continua sendo aplicada.
- Bloquear a utilizacao desse fluxo para alterar ou excluir o Super Administrador e preservar a trilha de auditoria das mudancas de perfil e acesso.
- Confirmar com produto e seguranca se os atalhos exigem confirmacao adicional, o efeito da transicao sobre sessoes ativas, tarefas, responsaveis, notificacoes, exportacoes e integracoes, e como o sistema trata secoes incompativeis com o novo perfil.

### Acessos de membros-usuarios

Com base no artigo [Definindo Acessos de Membros-Usuarios](https://intercom.help/compliasset/pt-BR/articles/5163738-definindo-acessos-de-membros-usuarios), publicado em 6 de setembro de 2024:

- o Membro-Administrador configura, supervisiona e gerencia o sistema; o Membro-Usuario auxilia na execucao das demandas, sem permissao para determinadas alteracoes e funcoes;
- somente o Membro-Administrador acessa `Configuracoes` pelo menu lateral;
- para alterar acessos de um Membro-Usuario, o Membro-Administrador acessa `Configuracoes` > `Membros`, localiza o membro e seleciona `Editar`;
- no perfil do Membro-Usuario, a area `Acessos` permite habilitar ou remover secoes visiveis, e a acao `Confirmar` salva a alteracao;
- habilitar uma secao torna todas as informacoes daquela secao visiveis ao Membro-Usuario;
- o sistema nao permite restringir o acesso a informacoes ou registros especificos dentro de uma secao habilitada;
- por exemplo, um Membro-Usuario com acesso a `Eventos` visualiza todos os eventos, inclusive os que contenham informacoes sigilosas; a mesma regra se aplica as demais secoes.

#### Como essa regra deve orientar um card

- Registrar o Membro-Usuario, a secao, a acao de habilitar ou remover, o Membro-Administrador responsavel, a data, o resultado salvo e o acesso efetivo antes e depois da mudanca.
- Tratar a concessao de uma secao como acesso amplo aos dados nela contidos; nao descrever ou aceitar filtragem por evento, documento, dossie ou outro registro individual sem uma funcionalidade formalmente definida.
- Classificar como risco de seguranca e privacidade qualquer solicitacao de acesso a uma secao que contenha dados sigilosos, avaliando se o perfil deve realmente receber toda a secao ou se a necessidade exige novo desenho de autorizacao.
- Validar que Membro-Usuario nao acessa `Configuracoes` e que apenas Membro-Administrador pode editar os acessos, inclusive por URL direta, API ou sessao ja ativa.
- Para remocao de acesso, testar o bloqueio imediato das telas, dados, exportacoes e acoes relacionadas, preservando o historico de auditoria da permissao revogada.
- Confirmar com produto e seguranca a lista de secoes atribuiveis, o comportamento para secoes novas, o tempo de revogacao em sessoes ativas, o alcance de exportacoes e integracoes e se ha excecoes ao modelo de acesso amplo por secao.

### Permissoes de acesso: usuario e administrador

Com base no artigo [Permissoes de Acesso: Usuario x Administrador](https://intercom.help/compliasset/pt-BR/articles/7231424-permissoes-de-acesso-usuario-x-administrador), publicado em 6 de abril de 2023, a matriz abaixo descreve as acoes de Membro-Usuario:

| Area | Criar | Editar | Excluir | Observacao |
|---|---|---|---|---|
| Atividade do Sistema | Nao | Sim | Nao | Apenas arquivar; criada internamente pelo time CompliAsset |
| Atividade Propria | Sim | Sim | Nao | Apenas arquivar |
| Obrigacao do Sistema | Nao | Nao | Nao | Apenas arquivar; criada internamente pelo time CompliAsset |
| Obrigacao Propria | Sim | Sim | Nao | Apenas arquivar |
| Eventos | Sim | Nao | Nao | |
| Colaboradores | Sim | Sim | Sim | |
| Fundos | Sim | Sim | Sim | |
| Investidores | Sim | Sim | Sim | |
| Terceiros | Sim | Sim | Nao | |
| Novo Documento | Sim | Nao | Nao | |
| Nova Versao de Documento | Nao | Nao | Nao | |
| Pasta de Documentos | Sim | Sim | Sim | |
| Aceites | Sim | Nao | Sim | |
| Treinamentos | Sim | Sim | Sim | |
| Planos de Acao | Sim | Sim | Sim | |
| Formularios | Sim | Sim | Sim | |

A matriz abaixo descreve as acoes de Membro-Administrador:

| Area | Criar | Editar | Excluir | Observacao |
|---|---|---|---|---|
| Atividade do Sistema | Nao | Sim | Nao | Apenas arquivar; criada internamente pelo time CompliAsset |
| Atividade Propria | Sim | Sim | Nao | Apenas arquivar |
| Obrigacao do Sistema | Nao | Nao | Nao | Apenas arquivar; criada internamente pelo time CompliAsset |
| Obrigacao Propria | Sim | Sim | Nao | Apenas arquivar |
| Eventos | Sim | Sim | Sim | |
| Colaboradores | Sim | Sim | Sim | |
| Fundos | Sim | Sim | Sim | |
| Investidores | Sim | Sim | Sim | |
| Terceiros | Sim | Sim | Sim | |
| Novo Documento | Sim | Sim | Sim | |
| Nova Versao de Documento | Sim | Sim | Sim | Ao excluir uma nova versao, a versao anterior volta a ser a original |
| Pasta de Documentos | Sim | Sim | Sim | |
| Aceites | Sim | Sim | Sim | |
| Treinamentos | Sim | Sim | Sim | |
| Planos de Acao | Sim | Sim | Sim | |
| Formularios | Sim | Sim | Sim | |

#### Como essa regra deve orientar um card

- Registrar o perfil, a area, a acao, a secao habilitada e o resultado esperado, distinguindo permissao de visualizacao por secao da permissao de criar, editar ou excluir.
- Para atividades e obrigacoes, tratar `arquivar` como acao distinta de excluir; nao aceitar exclusao quando a matriz indicar somente arquivamento.
- Preservar a criacao interna das Atividades e Obrigacoes do Sistema: nenhum perfil de Membro deve criar esses registros sem uma mudanca formal no processo do CompliAsset.
- Para documentos, separar novo documento, nova versao e pasta, pois as permissoes variam entre Membro-Usuario e Membro-Administrador; ao excluir nova versao como Administrador, validar o retorno da versao anterior ao estado original.
- Testar a matriz com secoes habilitadas e desabilitadas para Membro-Usuario, incluindo tentativas por URL direta, API, exportacao e sessao ativa, sem assumir que visibilidade da secao concede todas as acoes.
- Confirmar com produto e seguranca a vigencia da matriz, a definicao de atividades e obrigacoes proprias, o significado de arquivamento, a regra de Aceites, os efeitos de exclusao e o tratamento de permissoes em integracoes e sessoes existentes.

### FAQ financeiro e comercial

Com base no artigo [FAQ - Financeiro e Comercial](https://intercom.help/compliasset/pt-BR/articles/9659955-faq-financeiro-e-comercial), publicado em 29 de abril de 2026:

- cotacoes e demonstracoes devem ser solicitadas ao time de especialistas pelo canal comercial indicado no artigo;
- encerramento do contrato, encerramento de apenas um ambiente e revisao de contrato ou modulos devem ser tratados com `comercial@compliasset.com`;
- assuntos de contas a receber devem ser direcionados a `contasareceber@sinqia.com.br`, e assuntos de faturamento a `gestaodereceitas@sinqia.com.br`;
- a troca do e-mail de recebimento de notas fiscais deve ser solicitada a `gestaodereceitas@sinqia.com.br`;
- correcoes em notas fiscais devem ser tratadas pelos canais financeiros indicados;
- consultas do Dossie Reputacional do Data Engine nao estao incluidas na mensalidade: o artigo informa R$ 15 para CPF e R$ 25 para CNPJ, cobrados no mes seguinte;
- uma consulta solicitada nao pode ser cancelada; solicitacoes duplicadas para o mesmo nome e CPF ou CNPJ devem gerar apenas uma cobranca;
- consultas que retornarem erro ou arquivos incompletos nao devem ser cobradas; a cobranca se aplica as consultas que retornarem os dados;
- treinamentos sao contratados separadamente do software; e possivel manter uma conta apenas para treinamentos mesmo apos cancelar o sistema;
- clientes e nao-clientes podem solicitar treinamentos customizados com base em material enviado, pelo canal `treinamentos@compliasset.com`.

#### Como essa regra deve orientar um card

- Classificar a demanda como comercial, financeiro, consulta do Data Engine ou treinamento antes de encaminha-la.
- Nao colocar dados bancarios, documentos pessoais, valores de contratos ou informacoes fiscais sensiveis em cards sem necessidade; registrar somente o identificador da solicitacao e a evidencia minima.
- Para consultas do Dossie, registrar CPF ou CNPJ de forma mascarada, status do retorno, duplicidade, completude do arquivo e regra de cobranca aplicavel.
- Para cancelamento ou alteracao contratual, registrar se o pedido envolve o sistema inteiro, um ambiente, modulos especificos ou somente treinamentos, alem do canal responsavel.
- Nao assumir que valores, enderecos de e-mail, prazos de cobranca ou regras de cancelamento continuam atuais; confirmar com as areas responsaveis antes de transformar o artigo em criterio de aceite.
- Demandas de integracao devem separar o fluxo operacional do fornecedor financeiro, do comercial, do Data Engine e de treinamentos, com responsavel, entrada, saida e tratamento de falhas definidos.

### FAQ de treinamento na visao do colaborador

Com base no artigo [FAQ - Treinamento (Visao do Colaborador)](https://intercom.help/compliasset/pt-BR/articles/9682705-faq-treinamento-visao-do-colaborador), publicado em 5 de agosto de 2024:

- o progresso do treinamento e salvo quando o colaborador pausa e retoma o curso;
- o colaborador nao pode pular modulo ou topico: o proximo conteudo permanece bloqueado ate a conclusao do anterior;
- mesmo depois do prazo de conclusao, o treinamento continua acessivel enquanto a matricula estiver disponivel e dentro do ano em que a licenca foi adquirida;
- Estudos de Casos nao valem nota; somente as provas dos topicos `Vamos Testar Seu Conhecimento` sao avaliadas;
- e necessario atingir pelo menos 80% de acertos na prova para avancar ao proximo modulo;
- o gabarito exibido apos o teste corresponde as respostas dadas pelo colaborador, e nao necessariamente ao gabarito oficial;
- apos finalizar o treinamento, o sistema pode levar algum tempo para atualizar a porcentagem de conclusao e disponibilizar o certificado;
- para atingir 100%, o colaborador deve verificar se todos os indices de modulos e topicos estao completos e marcados em verde;
- depois da conclusao, o certificado fica disponivel para download no sistema.

#### Como essa regra deve orientar um card

- Registrar treinamento, matricula, modulo, topico, tentativa, percentual exibido, nota obtida, prazo da licenca e estado do certificado.
- Diferenciar progresso salvo, bloqueio por ordem de conteudo, nota de avaliacao, percentual de conclusao e disponibilidade do certificado.
- Para falhas de nota ou gabarito, guardar a prova e as respostas de forma controlada, sem expor dados pessoais desnecessarios, e confirmar qual gabarito oficial deve ser usado.
- Para divergencias de percentual ou certificado, verificar primeiro se todos os modulos e topicos estao completos e considerar eventual atraso de processamento antes de abrir um bug.
- Nao alterar a ordem obrigatoria ou o percentual minimo de 80% sem validar impacto em matriculas existentes, regras de avaliacao e certificados.
- Confirmar com produto o que significa matricula disponivel, como e calculado o ano da licenca, o tempo esperado de atualizacao, o criterio exato de 100% e a politica de novas tentativas.

### FAQ de treinamento na visao do usuario

Com base no artigo [FAQ - Treinamento (Visao do Usuario)](https://intercom.help/compliasset/pt-BR/articles/9714131-faq-treinamento-visao-do-usuario), publicado em 3 de março de 2026:

- as licencas de treinamento sao liberadas em ate dois dias uteis apos a contratacao e valem dentro do ano-calendario em que foram adquiridas;
- na virada do ano, as licencas sao removidas automaticamente e uma nova contratacao pode ser feita para o ano seguinte;
- os treinamentos `Dominando o Software` sao gratuitos;
- depois da matricula ou disparo, o treinamento fica imediatamente disponivel na visao do colaborador;
- e possivel atribuir o treinamento a `Todos os Colaboradores` ou a um grupo especifico;
- depois que um treinamento e iniciado pela tela `Novo Treinamento`, novas inclusoes e outras acoes devem ser feitas em `Todos os Treinamentos`;
- colaboradores atribuidos recebem por e-mail o convite e o link de acesso;
- o acompanhamento do progresso dos colaboradores ocorre em `Todos os Treinamentos`;
- uma licenca pode ser removida e reutilizada para outro colaborador somente enquanto o colaborador original ainda nao iniciou o treinamento;
- mesmo apos o prazo de conclusao, os colaboradores ainda conseguem acessar o treinamento;
- o prazo pode ser alterado em massa ou para um colaborador especifico, sem impactar os demais;
- e possivel reenviar o convite para colaboradores que ainda nao concluiram;
- divergencias no percentual de conclusao podem decorrer de atraso de atualizacao ou de modulos e topicos pendentes;
- o certificado fica disponivel automaticamente para download pelo colaborador e pelo membro, sem solicitacao;
- o certificado registra a conclusao do treinamento naquele ano e, conforme o artigo, nao possui prazo de validade;
- o artigo informa que o certificado e privado e nao possui convenio que lhe confira presuncao de validade perante CVM ou Anbima.

#### Como essa regra deve orientar um card

- Registrar contratacao, ano-calendario, quantidade de licencas, data de liberacao, treinamento, grupo ou colaborador, estado da matricula e prazo aplicavel.
- Diferenciar licenca contratada, matricula atribuida, treinamento iniciado, treinamento concluido, convite enviado e certificado disponibilizado.
- Para problemas de distribuicao, verificar permissao, grupo selecionado, treinamento ja iniciado, destinatarios, entrega do convite e disponibilidade na visao do colaborador.
- Para cancelamento ou transferencia de licenca, impedir a remocao depois do inicio sem uma regra confirmada de estorno, reutilizacao e preservacao do historico.
- Para prazos e progresso, registrar se a alteracao foi global ou individual e considerar processamento assincrono, modulos pendentes e impacto no certificado.
- Nao divulgar o certificado como acreditacao publica ou garantia de validade perante CVM, Anbima ou outro orgao sem validacao juridica e comercial especifica.
- Confirmar com produto e comercial os prazos de liberacao, regras de virada do ano, gratuidade, limites de grupos, permissoes do `membro`, reenvio de convites e politica de certificados.

### FAQ de aceites de documentos

Com base no artigo [FAQ - Aceites de Documentos](https://intercom.help/compliasset/pt-BR/articles/9925547-faq-aceites-de-documentos), publicado em 22 de agosto de 2025:

- uma campanha e criada em `Aceites de Documentos` > `Novo Aceite` e gera automaticamente um dossie de evento para acompanhamento;
- ao criar o Aceite, devem ser preenchidos natureza de Evento, data do ocorrido, data para conclusao, titulo, descricao e risco;
- e possivel anexar um ou mais documentos do computador ou da biblioteca de `Documentos`; campanhas sem anexos tambem podem ser criadas e enviadas para assinatura, mediante aviso antes da confirmacao;
- quando o Aceite possuir documento com link, o link nao e exibido no Evento da visao do Colaborador; para assegurar seu acesso, ele deve constar tambem na descricao do Aceite, e o sistema exibe aviso antes da criacao e envio;
- o mesmo documento pode ser enviado simultaneamente a todos os colaboradores usando o grupo `Todos os Colaboradores`;
- os arquivos podem ser organizados em pastas e subpastas na biblioteca de `Documentos` antes de serem selecionados para a campanha;
- a campanha aceita arquivos de documentos ou imagens, mas nao aceita audio ou video;
- ao enviar a campanha, o colaborador recebe uma notificacao por e-mail e visualiza o documento em sua visao de colaborador;
- o artigo classifica o aceite como assinatura eletronica simples, enquadrada no Art. 4o, I, da Lei no 14.063;
- cada aceite registra a validacao do usuario por login e senha, a sessao criada, numero de IP, localizacao com cidade, estado e pais e o momento em que a acao foi realizada;
- as evidencias da assinatura ficam gravadas junto ao aceite e armazenadas na auditoria do sistema, podendo ser solicitadas quando necessario;
- na visao de Colaborador, os Aceites pendentes ficam no cartao `Aceites de Documentos Pendentes`, que exibe os tres ultimos itens; `Ver Todos` abre os pendentes e concluidos;
- ao abrir o titulo de um Aceite, o modal apresenta suas informacoes e o documento; o Colaborador pode selecionar `x` para recusar, registrar que nao houve assinatura e seguir para justificativa;
- a recusa deve ser consultada no dossie do evento; recomenda-se que o Colaborador registre a justificativa em `Discussao`, mencione o time de compliance e que o responsavel altere o evento para `Nao realizado`, interrompendo os lembretes sobre o aceite;
- cada Colaborador recebe um Evento individual da campanha, permitindo que o Membro-Administrador consulte sua justificativa, acrescente consideracoes e mencione o Colaborador na resposta;
- o aceite pode ser enviado somente a colaboradores cadastrados em `Todos os Colaboradores`, nao a Terceiros;
- na criacao, os envolvidos podem ser Colaboradores ou Grupos compostos somente por Colaboradores; clientes e Terceiros nao podem ser adicionados;
- a opcao `Solicitar ao(s) envolvido(s) "Li, entendi e estou de acordo" no(s) documento(s) anexo(s)` vem selecionada e `Criar Evento` salva e envia a campanha;
- em uma campanha ja iniciada, novos Colaboradores podem ser incluidos por `Aceites de Documentos` > `Todos os Aceites` > `Adicionar Colaborador`, selecionando o nome, prazo limite para aceite e `Confirmar`;
- o Colaborador incluido recebe notificacao por e-mail e acessa a campanha pelo botao `Ver Documento(s)`;
- depois que a campanha foi criada e recebida pelos colaboradores, nao e possivel incluir ou excluir documentos; para atualizar o arquivo, deve ser criada nova campanha;
- aceites nao permitem campos adicionais de preenchimento; para isso, deve ser usado um `Formulario`, que tambem pode solicitar assinatura;
- no envio, ocorre uma notificacao; se o evento continuar pendente apos sete dias, sao enviadas cobrancas diarias ate a conclusao, e tambem existe a acao manual `Cobrar Atrasados`;
- em `Todos os Aceites`, e possivel exportar uma planilha Excel com as campanhas do sistema, gerar PDF, editar titulo, cobrar preenchimento, excluir campanha e adicionar Colaborador;
- ao abrir uma campanha, e possivel acompanhar por Colaborador o status do aceite, data de envio, prazo e situacao `Concluido`, `Atrasado` ou `Em Aberto`, reenviar convite a pendentes e removê-los da campanha;
- para remover um Colaborador, deve-se abrir a campanha em `Aceites de Documentos` > `Todos os Aceites`, localizar o nome, opcionalmente pela lupa, selecionar `Remover Colaborador` na linha correspondente e confirmar a exclusao;
- apos a confirmacao, o Colaborador e removido da campanha e a listagem e atualizada com os participantes atuais;
- a listagem de campanhas permite filtrar por status e situacao, incluindo pendente, aceito e recusado; o menu `Acoes` dentro da campanha repete as acoes individuais;
- os relatorios das campanhas devem seguir o fluxo documentado em `Exportacao de relatorios do sistema`.
- em `Todos os Aceites`, `Gerar PDF` ao lado do titulo da campanha produz relatorio com nome, descricao, categoria, data do primeiro envio, prazo de aceite, documentos submetidos e, para cada Colaborador, nome completo, status, data e hora da resposta e IP da resposta.

#### Como essa regra deve orientar um card

- Registrar campanha, natureza, datas, titulo, descricao, risco, documento ou link, versao, grupo ou destinatarios, evento gerado, status individual, data de envio e historico de notificacoes.
- Para campanhas com link ou sem anexos, registrar o aviso apresentado e validar que o link consta na descricao quando o acesso pelo Evento for necessario, sem assumir que o link anexado sera exibido ao Colaborador.
- Para inclusao posterior, registrar campanha, Colaborador, prazo limite, usuario que incluiu, data, notificacao enviada e disponibilidade de `Ver Documento(s)`, preservando os destinatarios e respostas anteriores.
- Para remocao de Colaborador, registrar campanha, participante, motivo, usuario responsavel, confirmacao, data e estado anterior e posterior da listagem, distinguindo a remocao individual da exclusao de toda a campanha.
- Para recusas, registrar campanha, Evento individual, Colaborador, momento da recusa, justificativa em `Discussao`, mencao ao time de compliance, responsavel pela analise e alteracao para `Nao realizado`, sem alterar o fato registrado.
- Testar o cartao `Aceites de Documentos Pendentes` com tres ou mais itens, `Ver Todos`, abertura do modal, recusa por `x`, inclusao de justificativa e interrupcao dos lembretes apos o tratamento do Evento.
- Permitir que Membro-Administrador analise e responda a recusa no dossie individual, mas nao permita que a resposta administrativa substitua, apague ou atribua ao Colaborador uma justificativa que ele nao enviou.
- Bloquear alteracoes retroativas nos documentos de campanhas ja recebidas, mas permitir a inclusao de Colaboradores conforme o fluxo documentado; mudancas de documento devem gerar nova campanha e manter o historico da anterior.
- Diferenciar aceite de documento, assinatura eletronica simples e formulario com campos de preenchimento; nao adicionar campos ao fluxo de aceite sem revisar o modulo correto.
- Para validar uma assinatura, conferir usuario autenticado, sessao, IP, localizacao e momento do aceite, vinculados ao documento, versao e campanha corretos, sem incluir esses dados sensiveis integralmente no card.
- Tratar IP, localizacao e dados de sessao como evidencias de seguranca e dados pessoais: restringir consulta, exportacao e compartilhamento, registrar finalidade e preservar mascaramento nas evidencias de atendimento.
- Para `Gerar PDF`, validar o escopo da campanha e o conteudo do relatorio; tratar nome completo, data e hora de resposta e IP como dados pessoais ou de seguranca e aplicar permissao, finalidade, minimizacao e controle de compartilhamento.
- Para cobrancas, validar o marco de sete dias, a periodicidade diaria, a condicao de parada e a acao manual `Cobrar Atrasados`.
- Validar busca pela lupa, `Remover Colaborador`, confirmacao e atualizacao da listagem, incluindo o efeito sobre o acesso do participante e suas notificacoes pendentes, sem remover outros participantes ou a campanha.
- Validar filtros, acompanhamento individual, reenvio de convite, remocao de Colaborador, edicao de titulo, cobranca, exclusao de campanha e equivalencia entre acoes da listagem e do menu `Acoes`, preservando documentos, respostas e historico conforme cada operacao.
- Nao tratar a classificacao juridica da assinatura como conclusao geral para todos os usos: confirmar com juridico o enquadramento legal, os requisitos de evidencia, a aplicacao por tipo de documento e a politica de retencao e disponibilizacao das evidencias de assinatura.
- Confirmar com produto os formatos aceitos, limites de tamanho, permissoes de destinatarios, comportamento do grupo `Todos os Colaboradores`, avisos para links e campanhas sem anexos, regras de inclusao posterior, prazo limite, reenvio, remocao e seus efeitos em acesso, lembretes e historico, exclusao de campanha, semantica da recusa por `x`, tratamento de lembretes, conteudo e acesso ao PDF e exportacao de relatorios.

### FAQ da biblioteca de documentos

Com base no artigo [FAQ - Biblioteca de Documentos](https://intercom.help/compliasset/pt-BR/articles/10539569-faq-biblioteca-de-documentos), publicado em 14 de fevereiro de 2025:

- a secao `Documentos` funciona como biblioteca para organizar e armazenar arquivos da empresa, como atas, politicas e manuais;
- a biblioteca permite compartilhar documentos para acesso e leitura, mas nao para coletar aceite; solicitacoes de assinatura devem usar `Aceites de Documentos`;
- links adicionados ao criar um documento ficam anexados como referencia; o sistema nao importa nem integra automaticamente o conteudo vinculado;
- a pasta principal e fixa e nao pode ser excluida;
- uma pasta criada pelo usuario pode ser classificada como `Principal`, funcionando como pasta mae, ou ser associada a uma pasta existente como subpasta; a criacao ocorre pela acao `+` > `Nova pasta`, seguida de nome, classificacao e `Confirmar`;
- uma pasta mae pode ser expandida para exibir e acessar suas subpastas;
- o cadastro de documento permite selecionar uma ou mais arquivos, informar um link publico em `Aponte aqui o Link`, escolher a pasta de destino ou, sem escolha, enviar o arquivo para a pasta principal do sistema;
- os metadados opcionais do documento incluem descricao, elaborado por, revisado por, aprovado por, data de vigencia e prazo de validade;
- o `Prazo de validade` pode ser informado na criacao ou na edicao de um documento e e salvo por `Carregar Documento`;
- documentos proximos ao prazo de validade geram alertas enviados junto ao Lembrete Semanal de Atividades e Eventos;
- ao habilitar `Visivel para Colaboradores`, todos os colaboradores cadastrados podem visualizar o documento, sem restricao por colaborador especifico;
- no cadastro em `Novo Documento`, a visibilidade e definida pela opcao `Visivel para Colaboradores` e salva por `Carregar Documento`;
- para documento existente, o usuario acessa `Todos os Documentos`, seleciona o titulo, usa `Editar`, habilita `Visivel para Colaboradores` e confirma em `Carregar Documento`;
- em `Todos os Documentos`, um Membro-Administrador pode selecionar o titulo e usar `Editar` para alterar titulo, descricao, pasta e adicionar ou remover arquivos; `Carregar Documento` salva essas alteracoes;
- colaboradores possuem acesso somente para leitura, sem editar ou excluir;
- somente Membros-Administradores podem editar e excluir documentos e enviar novas versoes;
- o acesso de Membros-Usuarios e controlado por seus perfis e permissoes, definidos pelos Membros-Administradores;
- usuarios com acesso apenas de Colaborador veem somente documentos marcados como `Visivel para Colaboradores`;
- na visao de Colaborador, os documentos visiveis ficam em `Biblioteca`; selecionar o titulo ou URL inicia o download automaticamente;
- Colaboradores veem os nomes de todas as pastas, mas so acessam o conteudo dos documentos marcados como visiveis;
- para Colaboradores ativos, a visibilidade concede acesso a ultima versao dos arquivos ou ao link do documento;
- a biblioteca aceita todos os formatos, exceto arquivos de video e audio;
- um documento enviado para assinatura fica vinculado ao evento da campanha e nao e salvo automaticamente na biblioteca;
- para atualizar uma versao, o usuario localiza a pasta e o documento em `Todos os Documentos`, seleciona seu titulo, usa `+`, inclui o arquivo em `Selecione o(s) Arquivo(s)` e salva por `Carregar Documento`;
- a tela de nova versao usa o mesmo formulario de cadastro de arquivo e tambem permite atualizar outras informacoes do documento;
- a acao `+`, ao lado de `Editar`, cria nova versao ao substituir o arquivo atual, sem agrupar os arquivos existentes; as versoes anteriores permanecem em `Versoes Anteriores` para consulta ou recuperacao e Colaboradores veem apenas a versao atual;
- `Versoes Anteriores` apresenta historico simplificado com numero de versoes, data de publicacao, usuario que publicou, descricao quando houver e arquivo para download ou URL;
- `Excluir` remove o documento inteiro de forma irreversivel, incluindo arquivos, versoes anteriores, comentarios em `Discussao` e demais historicos de movimentacao e interacao;
- para remover somente um arquivo, deve-se usar `Editar`, sem excluir o documento completo.
- uma pasta ou subpasta criada pode ter nome ou local alterado pelo icone de lapis; a exclusao pelo icone de lixeira de uma pasta mae remove tambem suas subpastas e arquivos.

#### Como essa regra deve orientar um card

- Diferenciar biblioteca, campanha de aceite e evento: armazenar um documento nao coleta assinatura, e enviar para aceite nao o adiciona automaticamente a biblioteca.
- Registrar documento, pasta, versao, origem do arquivo ou link, perfil do usuario, visibilidade e permissao efetiva ao investigar acesso ou versionamento.
- Nao tratar um link anexado como conteudo importado; validar separadamente disponibilidade, integridade e permissao de acesso ao destino externo.
- Distinguir a pasta principal fixa do sistema, que nao pode ser excluida, de uma pasta mae criada pelo usuario, cuja exclusao remove suas subpastas e arquivos.
- Para criar ou mover pastas, validar classificacao como pasta mae ou subpasta, nome, hierarquia, expansao e destino padrao do documento quando nenhuma pasta for selecionada.
- Registrar metadados informados e validar sua associacao ao documento, sem presumir que descricao, autoria, aprovacao, vigencia ou validade sao obrigatorios ou controlam automaticamente o acesso.
- Para o `Prazo de validade`, testar inclusao na criacao e edicao, persistencia por `Carregar Documento` e alerta no Lembrete Semanal para documento proximo ao vencimento.
- Distinguir alerta de validade de documento dos lembretes de Atividades e Eventos e nao assumir antecedencia, destinatarios adicionais ou bloqueio automatico do documento sem regra confirmada.
- Preservar a pasta principal e o historico de `Versoes Anteriores`; qualquer exclusao deve explicitar o risco de perda, a abrangencia em cascata e o impacto na auditoria.
- Distinguir edicao de informacoes, remocao de arquivo, criacao de nova versao e exclusao total; cada operacao deve ter criterios de aceite, auditoria e recuperacao proprios.
- Para nova versao, validar a localizacao pela pasta, o `+`, `Selecione o(s) Arquivo(s)` e `Carregar Documento`, a substituicao do arquivo atual sem agrupamento, a atualizacao de informacoes adicionais e a versao visivel para Colaboradores.
- Validar que `Versoes Anteriores` preserva numero, data de publicacao, usuario, descricao e arquivo ou URL da versao anterior, sem expor versoes nao autorizadas a Colaboradores.
- Para exclusao total, exigir confirmacao adequada e registrar que ela remove irreversivelmente arquivos, versoes, comentarios em `Discussao` e historico; para excluir um unico arquivo, validar o caminho por `Editar`.
- Para mudancas de visibilidade, considerar que `Visivel para Colaboradores` alcanca todos os colaboradores cadastrados e nao permite selecao individual.
- Testar a visibilidade tanto na criacao como na edicao do documento, validando `Carregar Documento`, a disponibilidade na `Biblioteca` e o download automatico por titulo ou URL.
- Validar que Colaboradores veem os nomes das pastas sem obter acesso ao conteudo de documentos nao visiveis, inclusive por URL direta ou tentativa de download.
- Para problemas de permissao, separar Membro-Administrador, Membro-Usuario e Colaborador e verificar a configuracao do perfil antes de alterar o documento.
- Confirmar com produto e seguranca os formatos realmente aceitos, comportamento de exclusao e recuperacao, limites de tamanho, acesso a links externos, funcionamento do download automatico, visibilidade de pastas, regras de metadados, antecedencia e destinatarios dos alertas de validade, diferenca entre pasta principal e pasta mae, exclusao em cascata, confirmacao de exclusao total, historico de versoes e regras de retencao.

### FAQ de formularios

Com base no artigo [FAQ - Formularios](https://intercom.help/compliasset/pt-BR/articles/11515925-faq-formularios), publicado em 16 de junho de 2025:

- depois de definir titulo, natureza do evento e descricao, e possivel personalizar os campos do formulario conforme as perguntas e respostas desejadas;
- um formulario pode ser editado depois de criado, mas as mudancas valem somente para novas campanhas; campanhas ja iniciadas mantem as perguntas originais;
- um mesmo formulario pode gerar campanhas de preenchimento varias vezes;
- criar e publicar o formulario nao solicita respostas automaticamente: e necessario iniciar uma campanha em `Todos os Formularios`;
- `Preenchimentos Isolados` ficam disponiveis para o colaborador responder a qualquer momento, sem uma solicitacao especifica, e servem para reportes recorrentes;
- esses formularios ficam em `Atalhos` na visao do colaborador e sao identificados pela tag `Formulario` na natureza do evento;
- cada solicitacao enviada por preenchimento isolado gera um evento individual, consultavel em `Todos os Eventos` ou em `Todos os Formularios` como `Preenchimentos Isolados`;
- formularios pendentes aparecem no painel `Preenchimento de Formularios Pendentes` ou no menu `Formularios` da visao do colaborador;
- um colaborador pode preencher novamente quando um membro envia nova solicitacao ou quando o formulario esta disponivel em `Atalhos`;
- depois do envio, as respostas nao podem ser editadas nem pelo colaborador nem pelo membro;
- em `Formularios` > `Todos os Formularios`, e possivel acompanhar campanhas, status, lembretes, novos colaboradores e relatorios;
- o sistema permite cobrar todos os nao respondidos, somente os nao respondidos atrasados ou usar `Cobrar Preenchimento` na campanha;
- respostas e preenchimentos dos colaboradores podem ser exportados em Excel.

#### Como essa regra deve orientar um card

- Registrar formulario, versao do modelo, campanha, colaborador, natureza do evento, origem normal ou isolada, status, prazo e momento do envio.
- Preservar a versao das perguntas para campanhas ja iniciadas; alteracoes no modelo nao devem modificar respostas ou perguntas historicas.
- Diferenciar formulario publicado, campanha iniciada, preenchimento pendente, preenchimento enviado e evento individual gerado por `Preenchimentos Isolados`.
- Para problemas de acesso, verificar se o formulario e pendente, se esta em `Atalhos`, se a campanha foi disparada e qual e a visao do usuario.
- Nao permitir edicao retroativa das respostas sem uma regra formal de correcao, auditoria e preservacao do valor originalmente enviado.
- Para lembretes, registrar o conjunto cobrado, a condicao de atraso, a data do envio e os destinatarios; evitar notificacoes duplicadas ou indevidas.
- Para exportacoes, considerar permissoes, escopo da campanha, respostas pessoais, formato Excel e protecao dos dados exportados.
- Confirmar com produto os tipos de campo, limites de repeticao, regras de prazo, comportamento de novas campanhas, identificacao de `Preenchimentos Isolados` e a politica de retencao das respostas.

### FAQ de customizacao de treinamentos

Com base no artigo [FAQ - Customizacao de Treinamentos](https://intercom.help/compliasset/pt-BR/articles/12291975-faq-customizacao-de-treinamentos), publicado em 17 de novembro de 2025:

- um treinamento proprio nao pode ser incluido diretamente pelo cliente; a inclusao e feita pelo time do Compliasset, que formata o material em modulos e topicos padronizados;
- podem ser usados textos, videos, imagens, gifs, telas interativas e outros materiais compatíveis com a plataforma;
- treinamentos customizados podem ser utilizados todos os anos, com licencas ilimitadas e sem prazo de validade; nova cobranca ocorre quando ha atualizacao de conteudo ou inclusao de novo treinamento;
- a customizacao envolve mensalidade de alocacao dos temas e trabalho de design e formatacao por hora, com minimo de tres horas, conforme analise do material;
- para clientes do Compliasset, o artigo informa cobranca apenas do trabalho de design e formatacao por hora;
- temas de prateleira tambem podem ser customizados, mediante contratacao do tema e cobranca do trabalho conforme o tipo e a quantidade de alteracoes;
- customizacao nao inclui criacao de novo conteudo: textos, roteiros e materiais devem ser fornecidos pela empresa contratante;
- o orcamento deve ser solicitado a `treinamentos@compliasset.com`, com `nathalia@compliasset.com` em copia, acompanhado do material e das dinamicas desejadas;
- exemplos de dinamicas a especificar incluem bloquear atalhos de avanco em videos e definir pontuacao minima para aprovacao em provas.

#### Como essa regra deve orientar um card

- Separar conteudo, design, formatacao, estrutura de modulos e topicos, perguntas, respostas, testes e certificados no escopo da demanda.
- Nao abrir card supondo que o cliente possa publicar o treinamento diretamente ou que a customizacao inclua redacao de novos textos, roteiros ou materiais.
- Registrar os arquivos fornecidos, formatos, versao do material, dinamicas desejadas, regras de avaliacao, prazo e responsavel pela aprovacao.
- Para atualizar um treinamento existente, verificar se a mudanca altera conteudo, design, perguntas, testes, certificado ou somente a apresentacao, preservando o historico e avaliando a nova cobranca.
- Para temas de prateleira, separar o custo e o escopo da contratacao original do custo e escopo das customizacoes solicitadas.
- Nao tratar valores, minimo de horas, licencas ilimitadas ou ausencia de prazo como condicoes contratuais definitivas sem confirmacao comercial vigente.
- Confirmar com produto e comercial os formatos suportados, o fluxo de envio e aprovacao, o ambiente de homologacao, limites tecnicos, prazo de entrega e criterios de aceite.

### FAQ de checklist

Com base no artigo [FAQ - Checklist](https://intercom.help/compliasset/pt-BR/articles/14669662-faq-checklist), publicado em 17 de abril de 2026:

- checklist divide uma demanda em tarefas menores, claras e rastreaveis dentro de um dossie, com responsavel, prazo e evidencias de execucao;
- checklists podem ser criados em `Agenda`, `Obrigacoes Estruturais`, `Eventos`, `Colaboradores` e `Terceiros`;
- membros podem criar e gerenciar checklists; colaboradores acessam apenas os checklists das tarefas pelas quais sao responsaveis;
- dentro do dossie, `Adicionar Checklist` cria a estrutura; depois e possivel adicionar tarefas, editar o titulo, excluir, cobrar itens nao respondidos ou atrasados e copiar ou substituir responsavel;
- substituir o responsavel diretamente na checklist altera todas as tarefas vinculadas, e nao somente uma tarefa;
- cada tarefa pode ter titulo, vencimento, descricao e responsaveis proprios, e uma checklist pode conter varias tarefas;
- na tarefa individual, e possivel consultar dados, adicionar comentarios em `Discussao`, concluir e usar `Acoes` para editar, cobrar ou excluir;
- para alterar o responsavel de uma unica tarefa, deve-se usar `Acoes` > `Editar Tarefa` dentro da tarefa;
- o menu lateral `Checklist` lista os itens organizados pela secao de origem e pelo dossie relacionado;
- os filtros disponiveis sao `Status`, `Secao`, `Responsavel` e `Titulo`, podendo ser combinados; status inclui atrasados, pendentes e concluidos;
- nao existe limite fixo de checklists ou tarefas por dossie, mas a organizacao e recomendada para evitar sobrecarga de visualizacao.

#### Como essa regra deve orientar um card

- Registrar dossie e secao de origem, checklist, tarefa, responsavel, prazo, descricao, evidencias, status e historico de alteracoes.
- Diferenciar acao no nivel da checklist da acao no nivel da tarefa, principalmente para substituicao de responsavel, cobranca, edicao e exclusao.
- Para mudancas de permissao, separar membro, colaborador responsavel e demais perfis, validando o acesso efetivo ao dossie e a tarefa.
- Preservar comentarios, conclusao, evidencias e historico quando uma tarefa ou responsavel for alterado.
- Para filtros e listagens, testar combinacoes de status, secao, responsavel e titulo, incluindo itens atrasados, pendentes e concluidos.
- Nao assumir que a ausencia de limite fixo elimina riscos de desempenho ou usabilidade; acompanhar volume, paginacao, ordenacao e tempo de carregamento.
- Confirmar com produto os criterios de permissao, notificacao e cobranca, comportamento ao excluir checklist ou tarefa, regras de prazo e tratamento de tarefas com multiplos responsaveis.

### Contratacao de treinamentos

Com base no artigo [Contratacao de Treinamentos](https://intercom.help/compliasset/pt-BR/articles/8496384-contratacao-de-treinamentos), publicado em 30 de janeiro de 2024:

- os temas de prateleira informados sao Anticorrupcao; ASG para Gestoras e Fundos; Ciberseguranca e Seguranca da Informacao; Conduta Etica no Trabalho; LGPD Basico para Colaboradores; LGPD para Encarregados e Colaboradores Diretamente Envolvidos em Protecao de Dados; Prevencao a Lavagem de Dinheiro e Financiamento ao Terrorismo; e Prevencao ao Insider Trading;
- a simulacao de valores e a contratacao sao feitas pelo link comercial indicado no artigo;
- e possivel contratar um combo ilimitado com todos os temas ou licencas individuais conforme quantidade e temas desejados;
- as licencas de treinamentos de prateleira valem por ano-calendario e ficam disponiveis ate 31 de dezembro do ano adquirido;
- informacoes adicionais sobre contratacao devem ser solicitadas a `comercial@compliasset.com`.

#### Como essa regra deve orientar um card

- Identificar se a demanda envolve treinamento de prateleira, combo, licenca individual ou treinamento customizado; nao misturar suas regras de validade e cobranca.
- Registrar temas, quantidade de licencas, ano de aquisicao, modalidade contratada, data de contratacao e ambiente ou grupo destinatario.
- Para problemas de disponibilidade, verificar se a licenca esta dentro do ano-calendario, se o tema foi contratado e se a quantidade de licencas foi consumida.
- Nao tratar a lista de temas, os valores, o conceito de ilimitado ou a validade como permanentes sem confirmacao comercial vigente.
- Confirmar com produto e comercial o link de simulacao, catalogo atual, regra de renovacao, comportamento em 31 de dezembro, transferencia de licencas e diferenca entre combo e licencas individuais.

### Processo de mapeamento de normas

Com base no artigo [Processo de Mapeamento de Normas](https://intercom.help/compliasset/pt-BR/articles/7280085-processo-de-mapeamento-de-normas), publicado em 17 de junho de 2025:

- o time de conteudo avalia diariamente publicacoes da CVM, ANBIMA, BCB e ANPD;
- no primeiro filtro, publicacoes pertinentes aos clientes sao selecionadas para o `Boletim Diario`, enquanto publicacoes de menor relevancia sao descartadas;
- o Boletim Diario entrega a informacao na origem e com celeridade;
- dentre as publicacoes do boletim, as que exigem aprofundamento podem gerar um `Alerta Regulatorio`, texto informativo elaborado pelo time de conteudo ou por escritorios parceiros;
- depois do alerta, e realizada uma `Analise de Impacto Regulatorio` para avaliar efeitos sobre a Agenda Regulatoria contratada;
- a analise pode editar atividades existentes, criar novas atividades ou excluir atividades quando um comando normativo for alterado, criado ou revogado;
- o trabalho de edicao, criacao e exclusao e descrito como manual e realizado por especialistas, com avaliacao tecnica de cada dispositivo;
- a analise tambem pode revisar categorias, consolidar obrigacoes repetitivas e reduzir pendencias quando houver sentido operacional;
- quando a alteracao for relevante, o time elabora um comunicado enviado com apoio do suporte aos clientes afetados.

#### Como essa regra deve orientar um card

- Diferenciar fonte regulatoria, publicacao original, item do Boletim Diario, Alerta Regulatorio, Analise de Impacto, atividade, obrigacao, categoria e comunicado ao cliente.
- Registrar regulador, identificador e data da publicacao, evidencia original, escopo da agenda contratada, analise realizada, decisao de editar/criar/excluir/consolidar e responsavel pela revisao.
- Nao tratar o Boletim Diario ou o Alerta Regulatorio como substitutos da norma original; preservar a fonte e deixar claro quando o conteudo e meramente informativo.
- Para alteracoes na Agenda, preservar historico, vinculo com a norma, estado anterior, estado novo, tarefas ja executadas, prazos e impacto nos clientes, com possibilidade de auditoria e recuperacao.
- Para exclusoes ou consolidacoes, verificar revogacao, duplicidade, equivalencia normativa, evidencias existentes e risco de apagar ou ocultar uma obrigacao ainda aplicavel.
- Nao assumir que toda publicacao gera atividade, alerta ou mudanca na agenda; registrar a justificativa do filtro e da analise de impacto.
- Separar automacao de ingestao, classificacao ou sugestao da decisao tecnica final; o artigo descreve edicao, criacao e exclusao manuais por especialistas.
- Confirmar com produto e conteudo os reguladores cobertos, criterios de relevancia, prazos de publicacao, regras de impacto, fluxo de aprovacao, comunicacao e tratamento de correcoes.

### Desbloqueio de acesso

Com base no artigo [Desbloqueio de Acesso](https://intercom.help/compliasset/pt-BR/articles/7860972-desbloqueio-de-acesso), publicado em 14 de agosto de 2024:

- depois de cinco tentativas de login sem sucesso, o usuario e automaticamente bloqueado;
- sem intervencao, o desbloqueio ocorre apos 24 horas;
- antes desse prazo, um Administrador deve acessar `Colaboradores` > `Todos os Colaboradores` > `Bloqueados`, localizar o colaborador e selecionar `Desbloquear`;
- apos o desbloqueio manual, o colaborador recebe um e-mail com a notificacao e um link para criar uma nova senha;
- usuarios recem-cadastrados entram automaticamente em `Bloqueados` e devem redefinir a senha no primeiro login;
- depois do login inicial e da redefinicao da senha, o usuario passa de `Bloqueados` para `Time Atual`;
- o colaborador recebe por e-mail os nomes dos administradores que podem ajudar no desbloqueio;
- todos os administradores da empresa sao notificados quando ocorre um bloqueio.

#### Como essa regra deve orientar um card

- Registrar a quantidade de tentativas, o horario do bloqueio, o perfil que executou o desbloqueio e o estado antes e depois da acao.
- Para falhas no fluxo, verificar separadamente bloqueio por tentativas excedidas, bloqueio inicial de cadastro, desbloqueio automatico, desbloqueio administrativo, envio do e-mail e redefinicao da senha.
- Nao permitir que uma melhoria remova o bloqueio ou a redefinicao obrigatoria sem avaliar o risco de ataques por tentativa, identidade e auditoria.
- Nao registrar senhas, links de redefinicao, tokens ou outros segredos em cards, anexos, logs de atendimento ou evidencias compartilhadas.
- Confirmar com produto e seguranca se o limite de cinco tentativas, o prazo de 24 horas, os destinatarios das notificacoes e a transicao para `Time Atual` permanecem iguais na versao atual.

### Reenvio de senha para colaborador

Com base no artigo [Reenvio de Senha para Colaborador](https://intercom.help/compliasset/pt-BR/articles/4583600-reenvio-de-senha-para-colaborador), publicado em 29 de abril de 2026:

- durante o cadastro de um colaborador, o sistema permite escolher se o e-mail de boas-vindas com as credenciais sera enviado naquele momento;
- se o envio nao ocorrer no cadastro, um Administrador pode acessar `Todos os Colaboradores`, abrir o perfil do colaborador e usar `Reenviar` para disparar o e-mail;
- o e-mail de reenvio contem credenciais e uma senha temporaria, que deve ser trocada imediatamente pelo colaborador;
- pela tela de login, qualquer pessoa pode selecionar `Esqueceu sua senha?`, informar o e-mail cadastrado e solicitar um link para criar uma nova senha;
- antes de solicitar a redefinicao, deve-se conferir se o e-mail foi cadastrado corretamente;
- se nenhuma das duas alternativas resultar no recebimento do e-mail, a orientacao e acionar o suporte pelo chat ou pelo e-mail `suporte@compliasset.com`.

#### Como essa regra deve orientar um card

- Diferenciar reenvio de credencial temporaria pelo perfil do colaborador e redefinicao iniciada na tela de login; nao tratar os dois fluxos como a mesma funcionalidade.
- Para bugs, registrar o perfil que iniciou a acao, o e-mail cadastrado, o tipo de mensagem esperado, o horario da solicitacao e o resultado da entrega, sem incluir senha ou link real.
- Preservar a obrigatoriedade de troca da senha temporaria e os controles de expiracao, uso unico e protecao contra abuso dos links de redefinicao.
- Avaliar com seguranca a informacao de que qualquer pessoa pode solicitar a redefinicao pela tela de login, evitando revelar se um e-mail esta cadastrado ou permitir abuso de envio.
- Confirmar com produto e seguranca se os nomes dos botoes, os perfis autorizados, o conteudo das mensagens, a validade da senha temporaria e o tratamento de falhas de entrega permanecem iguais na versao atual.

### Orientacoes para login

Com base no artigo [Orientacoes para Login](https://intercom.help/compliasset/pt-BR/articles/5183811-orientacoes-para-login), publicado em 29 de abril de 2026:

- diante das mensagens `Usuario ou Senha Invalidos` ou `Senha Expirada`, o usuario deve acessar `Esqueceu sua senha?`, informar o e-mail cadastrado e selecionar `Recuperar`;
- o sistema envia instrucoes e um link para criar uma nova senha; o cadastro correto do e-mail pode ser verificado pelo Administrador da empresa;
- a nova senha deve ter pelo menos oito caracteres, uma letra maiuscula, uma letra minuscula, um numero e um caractere especial;
- a senha nao pode comecar com um caractere especial;
- depois de repetir a senha e confirmar, o usuario deve utiliza-la no acesso seguinte;
- apos cinco tentativas incorretas, o acesso fica bloqueado e o usuario deve solicitar o desbloqueio ao time de compliance da empresa.

#### Como essa regra deve orientar um card

- Tratar a politica de senha como criterio objetivo de validacao: comprimento minimo, classes de caracteres exigidas e restricao para o primeiro caractere.
- Para bugs de login ou recuperacao, registrar a mensagem exibida, o fluxo utilizado, o resultado da validacao da senha e a entrega do e-mail, sem registrar a senha ou o link real.
- Diferenciar senha invalida, senha expirada e acesso bloqueado, pois cada situacao inicia um fluxo diferente.
- Há uma divergencia a confirmar com o artigo [Desbloqueio de Acesso](https://intercom.help/compliasset/pt-BR/articles/7860972-desbloqueio-de-acesso): este artigo orienta procurar o time de compliance, enquanto o anterior descreve desbloqueio por Administrador e desbloqueio automatico apos 24 horas. Nao transformar nenhum dos dois caminhos em criterio de aceite antes da confirmacao.
- Confirmar com produto e seguranca se os requisitos de senha, as mensagens, os nomes dos botoes, o perfil que pode verificar o e-mail e o fluxo de bloqueio permanecem iguais na versao atual.

### Validade de senhas para usuarios

Com base no artigo [Validade de Senhas para Usuarios](https://intercom.help/compliasset/pt-BR/articles/2856871-validade-de-senhas-para-usuarios), publicado em 29 de abril de 2026:

- ao redefinir a senha pela tela de login ou altera-la no proprio perfil, o usuario deve criar uma senha forte;
- a senha deve conter pelo menos uma letra minuscula, uma letra maiuscula, um numero, um caractere especial e oito caracteres;
- a nova senha deve ser diferente das senhas anteriores;
- um Administrador pode configurar a expiracao periodica das senhas para a equipe em `Configuracoes` > `Seguranca`, definindo a periodicidade e salvando a configuracao;
- senhas nao devem ser compartilhadas com terceiros ou informadas ao suporte, reutilizadas em outros sistemas ou anotadas em papel;
- a atualizacao regular e recomendada para reduzir vulnerabilidades.

#### Como essa regra deve orientar um card

- Validar a politica de senha nos dois caminhos descritos: recuperacao pela tela de login e alteracao dentro do perfil.
- Registrar como defeito qualquer aceite de senha que viole comprimento, classes de caracteres ou historico de senhas, sem incluir credenciais reais nas evidencias.
- Para demandas de expiracao, informar o administrador que alterou a configuracao, a periodicidade anterior e a nova, o escopo da equipe e o comportamento esperado para senhas ja expiradas.
- Considerar mensagens de orientacao, bloqueio de reutilizacao, privacidade, armazenamento seguro e impacto em autenticacao de dois fatores e sessoes ativas.
- Confirmar com produto e seguranca o numero de senhas anteriores que deve ser lembrado, as unidades aceitas para periodicidade, o prazo minimo e maximo e o comportamento apos a expiracao.

### Alteracao de senha

Com base no artigo [Alteracao de Senha](https://intercom.help/compliasset/pt-BR/articles/10069975-alteracao-de-senha), publicado em 29 de abril de 2026:

- dentro do sistema, o usuario acessa o menu com suas iniciais, seleciona `Alterar Senha`, informa a senha atual e digita duas vezes a nova senha;
- a nova senha deve conter pelo menos uma letra minuscula, uma letra maiuscula, um numero, um caractere especial, oito caracteres e ser diferente das anteriores;
- o usuario confirma a troca pelo botao `Trocar Senha`;
- fora do sistema, o usuario acessa `Esqueceu sua senha?` na tela de login, informa o e-mail cadastrado e usa o link recebido para redefinir a senha.

#### Como essa regra deve orientar um card

- Diferenciar alteracao autenticada, que exige a senha atual, de redefinicao por e-mail, que depende do link enviado ao endereco cadastrado.
- Para bugs, registrar o caminho utilizado, a etapa em que ocorreu a falha, a mensagem exibida e o resultado do envio ou da troca, sem expor senhas, links ou tokens.
- Reutilizar os criterios de senha forte documentados em `Validade de Senhas para Usuarios` e `Orientacoes para Login`, incluindo a verificacao do historico.
- Considerar o efeito da troca sobre autenticacao de dois fatores, sessoes ativas, recuperacao de acesso e notificacoes de seguranca.
- Confirmar com produto e seguranca se a senha atual e sempre obrigatoria no fluxo interno, se o link externo invalida sessoes anteriores e quais notificacoes devem ser enviadas apos a troca.

### Orientacoes para redefinicao de senha

Com base no artigo [Orientacoes para Alteracao de Senha](https://intercom.help/compliasset/pt-BR/articles/11589264-orientacoes-para-alteracao-de-senha#h_6042cd70b8), publicado em 30 de abril de 2026:

- a recuperacao deve ser solicitada no ambiente em que o usuario possui cadastro; se o ambiente estiver incorreto, o e-mail de redefinicao nao e enviado;
- o artigo relaciona `app.compliasset.com` a Empresas do Mercado de Capitais e Treinamentos, `payments.compliasset.com` a Instituicoes de Pagamentos e `previ.compliasset.com` a Empresas de Previdencia;
- na tela de login do ambiente correto, o usuario seleciona `Esqueceu sua senha?`, informa o e-mail cadastrado e seleciona `Recuperar`;
- antes de prosseguir, deve-se confirmar o e-mail cadastrado com o time de compliance quando houver duvida;
- o usuario deve conferir caixa de entrada e spam, abrir o link recebido e criar a nova senha conforme as regras vigentes;
- apos a alteracao, o sistema apresenta uma confirmacao na tela e envia uma confirmacao por e-mail; se isso nao ocorrer, o artigo orienta retornar a etapa anterior;
- para concluir o acesso, o usuario fecha a guia de confirmacao, abre a tela de login em nova janela ou guia, no ambiente correto, e entra com a nova senha;
- quando a empresa possuir ambiente separado, a orientacao e solicitar o link correto ao suporte.

#### Como essa regra deve orientar um card

- Registrar o ambiente e URL utilizados, etapa da redefinicao, mensagem exibida, estado de recebimento do e-mail e das confirmacoes e resultado do novo login, sem registrar senha, link, token ou e-mail completo.
- Validar que a solicitacao em ambiente incorreto nao envia e-mail e que a solicitacao no ambiente correto inicia o fluxo sem revelar se o endereco informado possui conta cadastrada.
- Testar separadamente recebimento do link, criacao de senha, confirmacao em tela, confirmacao por e-mail e login posterior em uma nova guia ou janela.
- Aplicar as regras de senha forte, expiracao, uso unico e protecao contra abuso documentadas nas demais secoes; a confirmacao de sucesso nao substitui a validacao de seguranca da nova senha.
- Ha divergencia de dominio para Previdencia: este artigo cita `previ.compliasset.com`, enquanto `FAQ de acesso e login` cita `abrapp.compliasset.com`; nao transformar nenhum desses enderecos em criterio de aceite sem confirmar o ambiente e a documentacao vigente.
- Confirmar com produto e seguranca os dominios por produto, a necessidade de abrir nova guia ou janela, o remetente e prazo do e-mail, as mensagens de confirmacao, invalidacao do link, protecao contra enumeracao de contas e o tratamento de ambientes separados.

### Exportacao de relatorios do sistema

Com base no artigo [Exportando Relatorios do Sistema](https://intercom.help/compliasset/pt-BR/articles/8842511-exportando-relatorios-do-sistema), publicado em 28 de junho de 2024:

- nas secoes de Atividades, Obrigacoes e Eventos, o usuario acessa `Toda(o)s`, pode aplicar filtros e usa `Exportar` para gerar uma planilha Excel;
- o mesmo fluxo de `Toda(o)s` e `Exportar` e apresentado para as bases de Colaboradores, Fundos, Investidores e Terceiros;
- em Aceite de Documentos, a tela `Todos os Aceites` permite gerar um PDF por campanha, pelo botao `Gerar PDF` ou pelo menu `Acoes` dentro da campanha;
- em Treinamentos, `Exportar` gera um relatorio das campanhas iniciadas e `Acoes` > `Gerar PDF` gera o relatorio individual de uma campanha;
- cada Plano de Acao gera um Evento, portanto seu relatorio deve seguir o fluxo de exportacao de Eventos;
- em Formulario, `Baixar Relatorio` permite escolher entre exportar as informacoes completas ou somente as respostas preenchidas, tanto na listagem geral quanto na campanha especifica;
- os relatorios exportados sao enviados por e-mail e tambem ficam centralizados em `Downloads` no menu esquerdo.
- apos selecionar `Exportar` em uma secao, o sistema exibe um modal de confirmacao e prepara o arquivo para envio;
- `Downloads` centraliza PDFs e planilhas exportados de modulos como Agenda, Colaboradores, Treinamentos e Aceites de Documentos;
- cada item em `Downloads` apresenta nome do arquivo, status, tamanho, data da transferencia e origem, indicando a pagina que emitiu o relatorio;
- a area `Downloads` de um usuario nao exibe arquivos solicitados por outros Membros do mesmo sistema.

#### Como essa regra deve orientar um card

- Registrar o modulo, a tela de origem, o tipo de arquivo esperado e se o relatorio e geral, filtrado ou individual.
- Para bugs de exportacao, informar filtros aplicados, campanha ou conjunto de registros, formato gerado, destinatario, confirmacao do modal e se o arquivo apareceu em `Downloads`.
- Nao assumir que todos os modulos usam o mesmo formato ou a mesma acao: o artigo diferencia planilha Excel, PDF, `Exportar` e `Baixar Relatorio`.
- Ao alterar relatorios, considerar escopo dos dados, permissoes, respostas preenchidas, envio por e-mail, centralizacao em `Downloads`, metadados do arquivo e rastreabilidade da exportacao.
- Validar que cada usuario visualiza somente seus proprios itens em `Downloads` e que a origem, status, tamanho e data correspondem ao arquivo solicitado, sem expor relatorios de outros Membros.
- Confirmar com produto se os nomes dos botoes, o comportamento dos filtros, os formatos, o modal, a disponibilidade em `Downloads`, a politica de retencao, o significado dos status e o comportamento de falha no envio de e-mail permanecem iguais na versao atual.

### Regra proposta para confirmacao de novo e-mail

Para permitir que o cliente altere o e-mail sem acionar o suporte, o novo endereco deve passar por confirmacao antes de substituir definitivamente o e-mail atual:

- ao informar um novo e-mail, o sistema deve marca-lo como **pendente de confirmacao**;
- o sistema deve enviar um token ou codigo de confirmacao para o novo e-mail;
- o novo e-mail so deve ser considerado valido e assumir o cadastro depois da confirmacao correta do token;
- enquanto a confirmacao nao ocorrer, o e-mail atual deve permanecer ativo para login e recebimento de comunicacoes;
- o token deve ser de uso unico, possuir prazo de expiracao e nao ser armazenado no card ou exposto em registros de atendimento;
- o usuario deve conseguir solicitar um novo token, respeitando limite de tentativas e reenvios;
- a alteracao confirmada deve gerar registro de auditoria com responsavel, data, horario, e-mail anterior e e-mail novo, sem registrar o token;
- se o token expirar ou for invalidado, a alteracao deve permanecer pendente ou ser cancelada, sem substituir o e-mail atual;
- o fluxo deve tratar o caso em que o novo e-mail ja esteja cadastrado em outra empresa contratante do CompliAsset;
- a implementacao deve definir como ficam a autenticacao de dois fatores, sessoes ativas, convites, notificacoes e recuperacao de senha apos a confirmacao.

Esta e uma regra proposta para a nova demanda e deve ser validada com produto, seguranca e tecnologia antes da implementacao. O token confirma o controle do novo endereco, mas nao substitui as demais validacoes de identidade, permissao e unicidade do e-mail.

## Tipos de card

Classifique a demanda antes de descreve-la:

- **Bug:** comportamento diferente do esperado ou erro que impede, prejudica ou distorce o uso.
- **Melhoria:** comportamento existente que pode ser mais simples, rapido, claro ou seguro.
- **Nova funcionalidade:** capacidade que ainda nao existe.
- **Demanda regulatoria:** necessidade decorrente de norma, prazo, obrigacao ou interpretacao regulatoria.
- **Investigacao:** duvida que precisa de analise antes de definir a solucao.
- **Tarefa tecnica:** trabalho interno necessario para sustentar uma entrega, integracao, dados, seguranca ou observabilidade.

## Template para abertura do card

Copie e preencha o modelo abaixo.

```md
# [TIPO] Titulo curto e orientado ao resultado

## Resumo
- **Tipo:** Bug | Melhoria | Nova funcionalidade | Demanda regulatoria | Investigacao | Tarefa tecnica
- **Modulo ou fluxo:**
- **Origem:** Cliente, operacao, produto, regulacao, suporte ou tecnologia
- **Solicitante:**
- **Prioridade sugerida:** Critica | Alta | Media | Baixa
- **Status da informacao:** Confirmada | Hipotese | Pendente de validacao

## Problema ou oportunidade
Descreva o que acontece hoje, quem e afetado, em qual contexto e qual prejuizo ou risco existe.

## Resultado esperado
Explique o que deve ser possivel fazer ou qual resultado deve ser obtido depois da entrega.

## Comportamento atual
- **Dado de entrada:**
- **Passos para reproduzir ou executar:**
- **Comportamento observado:**
- **Comportamento esperado:**

## Escopo inicial
### Inclui
- 

### Nao inclui
- 

## Regras de negocio e do sistema
- 

## Impactos a considerar
- **Usuario e experiencia:**
- **Permissoes e perfis:**
- **Dados e historico:**
- **Integracoes:**
- **Auditoria e evidencias:**
- **Notificacoes e prazos:**
- **Seguranca e privacidade:**

## Criterios de aceite
- [ ] 
- [ ] 
- [ ] 

## Evidencias
- **Artigo ou documentacao:**
- **Print, video ou log:**
- **Exemplo real:**
- **Card relacionado:**

## Duvidas e dependencias
- 

## Observacoes para implementacao
Registrar apenas decisoes ou restricoes ja confirmadas. Nao transformar hipotese tecnica em regra de negocio sem validacao.
```

## Regras para escrever bons cards

- Comece pelo problema e pelo resultado; nao comece pela tecnologia.
- Use um titulo que indique a acao ou o comportamento esperado.
- Separe fato observado, expectativa do usuario e hipotese de solucao.
- Informe sempre modulo, fluxo, perfil de usuario e cliente afetado quando aplicavel.
- Para bugs, inclua passos de reproducao, resultado atual e resultado esperado.
- Para demandas regulatorias, informe a fonte, o prazo, a obrigacao e o risco de nao atender.
- Para integracoes, registre sistema de origem, sistema de destino, evento, dados, autenticacao e tratamento de falhas.
- Para mudancas de dados, considere historico, migracao, exclusao, duplicidade e auditoria.
- Para cada criterio de aceite, descreva algo que possa ser verificado objetivamente.
- Nao misture varias demandas independentes no mesmo card; crie um card pai apenas quando houver uma relacao clara.

## Checklist antes de abrir

- [ ] O problema esta descrito com contexto suficiente?
- [ ] O modulo ou fluxo foi identificado?
- [ ] O tipo de card foi classificado?
- [ ] A fonte da informacao foi registrada?
- [ ] Fatos foram separados de hipoteses?
- [ ] O resultado esperado esta claro?
- [ ] Existem criterios de aceite verificaveis?
- [ ] Foram considerados permissoes, auditoria, dados e notificacoes?
- [ ] Dependencias e duvidas estao explicitas?
- [ ] A demanda pode ser entendida sem depender de uma conversa oral?

## Como pedir ajuda a partir deste MD

Ao solicitar apoio para criar ou revisar um card, forneca:

1. este documento como contexto;
2. os artigos relacionados ao modulo ou fluxo;
3. a descricao bruta da necessidade;
4. evidencias disponiveis;
5. o que ja foi confirmado e o que ainda e suposicao.

A resposta deve preservar as regras documentadas, sinalizar contradicoes, fazer perguntas somente quando forem necessarias e nao inventar comportamento do sistema.

## Controle da base de conhecimento

Mantenha abaixo um indice dos materiais incorporados.

Use os status desta forma:

- **Vigente confirmado:** regra validada com a versao atual do produto ou com a area responsavel.
- **Vigente a confirmar:** descrita em fonte oficial, mas ainda nao validada quanto a sua vigencia atual.
- **Historico:** material mantido para contexto, mas que nao deve orientar sozinho um novo card.
- **Pendente:** material recebido, mas ainda nao analisado ou sem informacao suficiente.

| ID | Material | Assunto | Status | Data de consulta | Observacao |
|---|---|---|---|---|---|
| ART-001 | [Alteracao de Nomes e E-mails de Colaboradores](https://intercom.help/compliasset/pt-BR/articles/4789039-alteracao-de-nomes-e-e-mails-de-colaboradores) | Seguranca e cadastro de colaboradores | Vigente a confirmar | 2026-09-02 | Publicado em 26/04/2023; regra de alteracao de nome requer confirmacao |
| ART-002 | [Autenticacao de Dois Fatores](https://intercom.help/compliasset/pt-BR/articles/1956042-autenticacao-de-dois-fatores) | Seguranca e acesso | Vigente a confirmar | 2026-09-02 | Publicado em 02/05/2023; confirmar se o fluxo atual permanece igual |
| ART-003 | [Exportando Relatorios do Sistema](https://intercom.help/compliasset/pt-BR/articles/8842511-exportando-relatorios-do-sistema) | Relatorios e downloads | Vigente a confirmar | 2026-09-03 | Publicado em 28/06/2024; confirmar botoes, formatos, filtros, envio por e-mail e centralizacao em `Downloads` |
| ART-004 | [Desbloqueio de Acesso](https://intercom.help/compliasset/pt-BR/articles/7860972-desbloqueio-de-acesso) | Seguranca, login e senhas | Vigente a confirmar | 2026-09-03 | Publicado em 14/08/2024; confirmar limite, prazo, notificacoes e redefinicao obrigatoria |
| ART-005 | [Reenvio de Senha para Colaborador](https://intercom.help/compliasset/pt-BR/articles/4583600-reenvio-de-senha-para-colaborador) | Seguranca, login e senhas | Vigente a confirmar | 2026-09-03 | Publicado em 29/04/2026; confirmar perfis, mensagens, expiracao e protecoes contra abuso |
| ART-006 | [Orientacoes para Login](https://intercom.help/compliasset/pt-BR/articles/5183811-orientacoes-para-login) | Seguranca, login e senhas | Vigente a confirmar | 2026-09-03 | Publicado em 29/04/2026; confirmar politica de senha e divergencia no fluxo de desbloqueio |
| ART-007 | [Validade de Senhas para Usuarios](https://intercom.help/compliasset/pt-BR/articles/2856871-validade-de-senhas-para-usuarios) | Seguranca, login e senhas | Vigente a confirmar | 2026-09-03 | Publicado em 29/04/2026; confirmar historico de senhas e parametros de expiracao |
| ART-008 | [Alteracao de Senha](https://intercom.help/compliasset/pt-BR/articles/10069975-alteracao-de-senha) | Seguranca, login e senhas | Vigente a confirmar | 2026-09-03 | Publicado em 29/04/2026; confirmar diferenca entre troca interna e redefinicao externa |
| ART-009 | [FAQ - Acesso e Login](https://intercom.help/compliasset/pt-BR/articles/9641358-faq-acesso-e-login) | Seguranca, login, ambientes e perfis | Vigente a confirmar | 2026-09-03 | Publicado em 05/03/2026; confirmar links, metodos de login, mensagens de erro e responsavel pelo desbloqueio |
| ART-010 | [FAQ - Cadastros de Colaboradores](https://intercom.help/compliasset/pt-BR/articles/9653170-faq-cadastros-de-colaboradores) | Cadastros, identidade e acesso | Vigente a confirmar | 2026-09-03 | Publicado em 29/07/2024; confirmar importacao, identificador por e-mail, eventos automaticos e estados do colaborador |
| ART-011 | [FAQ - Financeiro e Comercial](https://intercom.help/compliasset/pt-BR/articles/9659955-faq-financeiro-e-comercial) | Contratos, financeiro, Data Engine e treinamentos | Vigente a confirmar | 2026-09-03 | Publicado em 29/04/2026; confirmar contatos, valores, cobranca e regras de cancelamento |
| ART-012 | [FAQ - Treinamento (Visao do Colaborador)](https://intercom.help/compliasset/pt-BR/articles/9682705-faq-treinamento-visao-do-colaborador) | Treinamentos, avaliacao e certificados | Vigente a confirmar | 2026-09-03 | Publicado em 05/08/2024; confirmar matricula, nota minima, processamento e criterios de conclusao |
| ART-013 | [FAQ - Treinamento (Visao do Usuario)](https://intercom.help/compliasset/pt-BR/articles/9714131-faq-treinamento-visao-do-usuario) | Treinamentos, licencas, prazos e certificados | Vigente a confirmar | 2026-09-03 | Publicado em 03/03/2026; confirmar licencas, permissoes, transferencia e comunicacao sobre certificados |
| ART-014 | [FAQ - Aceites de Documentos](https://intercom.help/compliasset/pt-BR/articles/9925547-faq-aceites-de-documentos) | Aceites, assinaturas, eventos e notificacoes | Vigente a confirmar | 2026-09-03 | Publicado em 22/08/2025; confirmar formatos, imutabilidade, cobrancas e enquadramento juridico |
| ART-015 | [FAQ - Biblioteca de Documentos](https://intercom.help/compliasset/pt-BR/articles/10539569-faq-biblioteca-de-documentos) | Biblioteca, documentos, versoes e permissoes | Vigente a confirmar | 2026-09-03 | Publicado em 14/02/2025; confirmar visibilidade, formatos, exclusao, recuperacao e retencao |
| ART-016 | [FAQ - Formularios](https://intercom.help/compliasset/pt-BR/articles/11515925-faq-formularios) | Formularios, campanhas, eventos e respostas | Vigente a confirmar | 2026-09-03 | Publicado em 16/06/2025; confirmar versionamento, preenchimentos isolados, cobrancas e exportacao |
| ART-017 | [FAQ - Customizacao de Treinamentos](https://intercom.help/compliasset/pt-BR/articles/12291975-faq-customizacao-de-treinamentos) | Treinamentos, customizacao, conteudo e custos | Vigente a confirmar | 2026-09-03 | Publicado em 17/11/2025; confirmar formatos, escopo, licencas, valores e prazo de entrega |
| ART-018 | [FAQ - Checklist](https://intercom.help/compliasset/pt-BR/articles/14669662-faq-checklist) | Checklists, tarefas, responsabilidades e prazos | Vigente a confirmar | 2026-09-03 | Publicado em 17/04/2026; confirmar permissoes, propagacao de responsavel, filtros e exclusao |
| ART-019 | [Contratacao de Treinamentos](https://intercom.help/compliasset/pt-BR/articles/8496384-contratacao-de-treinamentos) | Treinamentos de prateleira, licencas e contratacao | Vigente a confirmar | 2026-09-03 | Publicado em 30/01/2024; confirmar catalogo, combo, valores, validade e renovacao |
| ART-020 | [Processo de Mapeamento de Normas](https://intercom.help/compliasset/pt-BR/articles/7280085-processo-de-mapeamento-de-normas) | Conteudo regulatorio, alertas e Agenda | Vigente a confirmar | 2026-09-03 | Publicado em 17/06/2025; confirmar fontes, filtros, analise de impacto, revisoes e comunicados |
| ART-021 | [Explorando a Secao 'Visual'](https://intercom.help/compliasset/pt-BR/articles/7947430-explorando-a-secao-visual) | Identidade visual, canais, PDFs e e-mails | Vigente a confirmar | 2026-09-03 | Publicado em 03/04/2025; confirmar formatos processados, permissoes, publicacao, propagacao e historico |
| ART-022 | [Guia de Primeiro Acesso](https://intercom.help/compliasset/pt-BR/articles/6695329-guia-de-primeiro-acesso) | Primeiro acesso, credenciais temporarias e recuperacao de senha | Vigente a confirmar | 2026-09-03 | Publicado em 29/04/2026; confirmar remetente, dominios, provedores de login e protecoes de recuperacao |
| ART-023 | [Cadastro de Membros](https://intercom.help/compliasset/pt-BR/articles/1948899-cadastro-de-membros) | Membros, perfis e permissoes de acesso | Vigente a confirmar | 2026-09-03 | Publicado em 18/04/2024; confirmar matriz de acesso, responsaveis pela gestao e efeitos da reversao |
| ART-024 | [Configuracoes do Perfil](https://intercom.help/compliasset/pt-BR/articles/4360165-configuracoes-do-perfil) | Meu Perfil, preferencias e seguranca de membros | Vigente a confirmar | 2026-09-03 | Publicado em 22/11/2024; confirmar limites, sessoes, lembretes e diferencas para colaboradores |
| ART-025 | [Definindo Acessos de Membros-Usuarios](https://intercom.help/compliasset/pt-BR/articles/5163738-definindo-acessos-de-membros-usuarios) | Perfis, permissoes e visibilidade por secao | Vigente a confirmar | 2026-09-03 | Publicado em 06/09/2024; confirmar secoes atribuiveis, revogacao e ausencia de restricao por registro |
| ART-026 | [Permissoes de Acesso: Usuario x Administrador](https://intercom.help/compliasset/pt-BR/articles/7231424-permissoes-de-acesso-usuario-x-administrador) | Matriz de criar, editar, excluir e arquivar por perfil | Vigente a confirmar | 2026-09-03 | Publicado em 06/04/2023; confirmar a matriz, arquivamento, Aceites e versionamento de documentos |
| ART-027 | [Grupos, Departamentos e Funcoes](https://intercom.help/compliasset/pt-BR/articles/6808185-grupos-departamentos-e-funcoes) | Classificacao de colaboradores e selecao em massa | Vigente a confirmar | 2026-09-03 | Publicado em 20/06/2024; confirmar permissoes, exclusao, historico e impacto em Eventos |
| ART-028 | [Navegar entre Empresas](https://intercom.help/compliasset/pt-BR/articles/5117898-navegar-entre-empresas) | Ambientes, Membros e Colaboradores | Vigente a confirmar | 2026-09-03 | Publicado em 06/12/2023; confirmar elegibilidade, sessao, isolamento e auditoria da troca |
| ART-029 | [Organizacao em Grupos](https://intercom.help/compliasset/pt-BR/articles/2169967-organizacao-em-grupos#h_b323b039e9) | Grupos, participantes e importacao CSV | Vigente a confirmar | 2026-09-03 | Publicado em 17/11/2025; confirmar modelo, codificacao, limites, processamento e impactos em Eventos |
| ART-030 | [Definicao dos Perfis de Acessos](https://intercom.help/compliasset/pt-BR/articles/1956039-definicao-dos-perfis-de-acessos) | Perfis, administracao e governanca de acesso | Vigente a confirmar | 2026-09-03 | Publicado em 08/08/2025; confirmar matriz atual, troca do Super Administrador e limites de edicao |
| ART-031 | [Alterar Perfis de Acesso](https://intercom.help/compliasset/pt-BR/articles/4680531-alterar-perfis-de-acesso) | Alteracao de perfis e acessos de membros | Vigente a confirmar | 2026-09-03 | Publicado em 22/12/2023; confirmar atalhos, persistencia, revogacao e efeitos em sessoes |
| ART-032 | [Gerenciar as Notificacoes](https://intercom.help/compliasset/pt-BR/articles/4931000-gerenciar-as-notificacoes) | Caixa de entrada, leitura e acoes em lote | Vigente a confirmar | 2026-09-03 | Publicado em 20/06/2025; confirmar retencao, exclusao, sincronizacao e permissoes de dossies |
| ART-033 | [Historico de Acessos](https://intercom.help/compliasset/pt-BR/articles/4335645-historico-de-acessos) | Auditoria de acessos, IP e localizacao | Vigente a confirmar | 2026-09-03 | Publicado em 26/01/2026; confirmar retencao, exportacao, geolocalizacao e controles de privacidade |
| ART-034 | [Ativar Lembretes por E-mail](https://intercom.help/compliasset/pt-BR/articles/7946246-ativar-lembretes-por-e-mail) | Lembretes semanais e personalizados | Vigente a confirmar | 2026-09-03 | Publicado em 24/02/2026; confirmar ativacao, horarios, escopo, destinatarios e entrega |
| ART-035 | [API Token](https://intercom.help/compliasset/pt-BR/articles/8141236-api-token) | Tokens, documentacao e integracoes de API | Vigente a confirmar | 2026-09-03 | Publicado em 19/07/2023; confirmar perfis, escopos, rotacao, revogacao e auditoria |
| ART-036 | [Entendendo a Estruturacao do Sistema](https://intercom.help/compliasset/pt-BR/articles/8330876-entendendo-a-estruturacao-do-sistema) | Estrutura do sistema, dossies, relacionados e campanhas | Vigente a confirmar | 2026-09-03 | Publicado em 03/06/2026; confirmar status, fluxos de campanha e regras de Relacionados |
| ART-037 | [Guia de Primeiros Passos](https://intercom.help/compliasset/pt-BR/articles/8727731-guia-de-primeiros-passos) | Onboarding, carga inicial e inicio da operacao | Vigente a confirmar | 2026-09-03 | Publicado em 21/12/2023; roteiro recomendado, confirmar obrigatoriedades e fluxos por ambiente |
| ART-038 | [6 Funcoes Uteis no Compliasset](https://intercom.help/compliasset/pt-BR/articles/9200338-6-funcoes-uteis-no-compliasset) | Configuracoes internas, status, eventos e lembretes | Vigente a confirmar | 2026-09-03 | Publicado em 18/04/2024; confirmar ativacao interna, regras de status e Enquadramento |
| ART-039 | [Atribuicoes do Super Administrador](https://intercom.help/compliasset/pt-BR/articles/9298311-atribuicoes-do-super-administrador) | Responsabilidades, comunicacoes e canais de suporte | Vigente a confirmar | 2026-09-03 | Publicado em 02/06/2026; confirmar responsabilidades, comunicacoes e canais vigentes |
| ART-040 | [Atribuicoes dos Membros](https://intercom.help/compliasset/pt-BR/articles/9331529-atribuicoes-dos-membros) | Responsabilidades, perfis e comunicacoes de membros | Vigente a confirmar | 2026-09-03 | Publicado em 16/05/2024; confirmar responsabilidades e matriz de permissoes vigente |
| ART-041 | [Explorando 'Configuracoes'](https://intercom.help/compliasset/pt-BR/articles/8985454-explorando-configuracoes) | Governanca de configuracoes, canais e naturezas | Vigente a confirmar | 2026-09-03 | Publicado em 27/02/2024; confirmar submodulos, auditoria, Canais e Naturezas de Eventos |
| ART-042 | [Explorando Downloads](https://intercom.help/compliasset/pt-BR/articles/9516483-explorando-downloads) | Exportacoes, e-mail e area pessoal de Downloads | Vigente a confirmar | 2026-09-03 | Publicado em 25/06/2024; confirmar status, retencao, entrega e isolamento por usuario |
| ART-043 | [Remover Acesso de Membro](https://intercom.help/compliasset/pt-BR/articles/9619968-remover-acesso-de-membro) | Desligamento, acesso e historico de membros | Vigente a confirmar | 2026-09-03 | Publicado em 19/07/2024; confirmar bloqueio, recontratacao, responsabilidades e retencao |
| ART-044 | [Alteracao de Pessoa de Contato](https://intercom.help/compliasset/pt-BR/articles/9949044-alteracao-de-pessoa-de-contato) | Canal de Compliance, contatos e notificacoes | Vigente a confirmar | 2026-09-03 | Publicado em 07/10/2024; confirmar elegibilidade, notificacoes, historico e publicacao |
| ART-045 | [Navegando entre Visao de Usuario e Colaborador](https://intercom.help/compliasset/pt-BR/articles/6032604-navegando-entre-visao-de-usuario-e-colaborador) | Alternancia de visao, treinamentos e formularios | Vigente a confirmar | 2026-09-03 | Publicado em 28/04/2025; confirmar elegibilidade, sessao, auditoria e contexto de dados |
| ART-046 | [Orientacoes para Alteracao de Senha](https://intercom.help/compliasset/pt-BR/articles/11589264-orientacoes-para-alteracao-de-senha#h_6042cd70b8) | Redefinicao de senha, dominios e confirmacoes | Vigente a confirmar | 2026-09-03 | Publicado em 30/04/2026; confirmar dominios de Previdencia, fluxo de confirmacao e seguranca |
| ART-047 | [Navegacoes de Usuarios](https://intercom.help/compliasset/pt-BR/articles/16680587-navegacoes-de-usuarios) | Auditoria de uso, filtros e exportacao individual | Vigente a confirmar | 2026-09-03 | Atualizado na semana de consulta; confirmar retencao, granularidade, exportacao e privacidade |
| ART-048 | [Canais de Ajuda](https://intercom.help/compliasset/pt-BR/articles/6826944-canais-de-ajuda) | Suporte, Central de Ajuda, noticias e treinamentos | Vigente a confirmar | 2026-09-03 | Publicado em 23/04/2026; confirmar horarios, disponibilidade, retencao e condicoes de treinamento |
| ART-049 | [Notas de Atualizacao e Correcoes](https://intercom.help/compliasset/pt-BR/articles/7904227-notas-de-atualizacao-e-correcoes) | Noticias, atualizacoes e correcoes do sistema | Vigente a confirmar | 2026-09-03 | Publicado em 07/03/2025; confirmar cadencia, escopo e link externo vigente |
| ART-050 | [Novos Cartoes no Dashboard](https://intercom.help/compliasset/pt-BR/articles/7173226-novos-cartoes-no-dashbord) | Dashboard, modulos regulatorios e categorias | Vigente a confirmar | 2026-09-03 | Publicado em 22/03/2023; confirmar calculos, filtros, visibilidade e versao atual |
| ART-051 | [Customizando o Dashboard](https://intercom.help/compliasset/pt-BR/articles/2047898-customizando-o-dashboard) | Preferencias, filtros e cartoes do Dashboard | Vigente a confirmar | 2026-09-03 | Publicado em 01/08/2024; confirmar persistencia, filtros e criacao de cartoes |
| ART-052 | [Adicionar Filtro no Dashboard](https://intercom.help/compliasset/pt-BR/articles/4951524-adicionar-filtro-no-dashboard) | Cartoes por filtros de Agenda e Eventos | Vigente a confirmar | 2026-09-03 | Publicado em 16/05/2024; confirmar filtros, limites, persistencia e comportamento de `Ver mais` |
| ART-053 | [Navegando pelo Dashboard](https://intercom.help/compliasset/pt-BR/articles/7125299-navegando-pelo-dashboard) | Cartoes operacionais, riscos e pendencias | Vigente a confirmar | 2026-09-03 | Publicado em 24/06/2024; confirmar cartoes, fontes, cores, ordenacao e permissoes |
| ART-054 | [Tour pelo Calendario do Dashboard](https://intercom.help/compliasset/pt-BR/articles/8576396-tour-pelo-calendario-do-dashboard) | Calendario, responsaveis, status e dossies | Vigente a confirmar | 2026-09-03 | Publicado em 04/04/2025; confirmar cores, filtros, datas e navegacao entre secoes |
| ART-055 | [Documentos Visiveis para Colaboradores](https://intercom.help/compliasset/pt-BR/articles/4377193-documentos-visiveis-para-colaboradores) | Biblioteca, visibilidade e download de documentos | Vigente a confirmar | 2026-09-03 | Publicado em 29/08/2024; confirmar publicacao, pastas, download e permissoes |
| ART-056 | [Organizacao da Biblioteca de Documentos](https://intercom.help/compliasset/pt-BR/articles/2460218-organizacao-da-biblioteca-de-documentos) | Pastas, metadados e exclusao de documentos | Vigente a confirmar | 2026-09-03 | Publicado em 25/06/2026; confirmar hierarquia, exclusao em cascata e retencao |
| ART-057 | [Editando e Excluindo Documentos](https://intercom.help/compliasset/pt-BR/articles/9588521-editando-e-excluindo-documentos) | Edicao, versoes e exclusao de documentos | Vigente a confirmar | 2026-09-03 | Publicado em 23/06/2026; confirmar exclusao irreversivel, versoes e auditoria |
| ART-058 | [Nova Versao de Documentos](https://intercom.help/compliasset/pt-BR/articles/10511975-nova-versao-de-documentos) | Atualizacao e historico de versoes | Vigente a confirmar | 2026-09-03 | Publicado em 24/06/2026; confirmar metadados, historico, permissao e visibilidade |
| ART-059 | [Prazo de Validade em Documentos](https://intercom.help/compliasset/pt-BR/articles/12691661-prazo-de-validade-em-documentos) | Validade de documentos e alertas semanais | Vigente a confirmar | 2026-09-03 | Publicado em 28/11/2025; confirmar antecedencia, destinatarios e comportamento apos vencimento |
| ART-060 | [Validacao de Assinaturas](https://intercom.help/compliasset/pt-BR/articles/6153683-validacao-de-assinaturas) | Aceites, evidencias de assinatura e auditoria | Vigente a confirmar | 2026-09-03 | Publicado em 26/01/2024; confirmar retencao, acesso e enquadramento juridico |
| ART-061 | [Adicionar Colaborador em Aceites de Documentos](https://intercom.help/compliasset/pt-BR/articles/4930262-adicionar-colaborador-em-aceites-de-documentos) | Inclusao posterior, notificacao e PDF de Aceites | Vigente a confirmar | 2026-09-03 | Publicado em 26/05/2025; confirmar prazos, permissoes, PDF e privacidade |
| ART-062 | [Aceites de Documentos](https://intercom.help/compliasset/pt-BR/articles/7938792-aceites-de-documentos) | Criacao, acompanhamento e acoes de campanhas | Vigente a confirmar | 2026-09-03 | Publicado em 30/09/2025; confirmar avisos, acoes, filtros e exclusao de campanha |
| ART-063 | [Recusa de Aceite de Documentos](https://intercom.help/compliasset/pt-BR/articles/9822903-recusa-de-aceite-de-documentos) | Recusa, justificativa e tratamento de Aceites | Vigente a confirmar | 2026-09-03 | Publicado em 09/09/2024; confirmar semantica da recusa, lembretes e permissoes |
| ART-064 | [Remover Colaborador de Aceite de Documento](https://intercom.help/compliasset/pt-BR/articles/11602780-remover-colaborador-de-aceite-de-documento) | Remocao individual de participantes de Aceites | Vigente a confirmar | 2026-09-03 | Publicado em 20/06/2025; confirmar permissoes, efeitos em acesso, lembretes e historico |
| ART-065 | [Upload de Novos Participantes](https://intercom.help/compliasset/pt-BR/articles/8095579-upload-de-novos-participantes) | Importacao em massa de participantes por CSV | Vigente a confirmar | 2026-09-10 | Publicado em 05/07/2023; confirmar identificacao de registros, atualizacao, limites, permissao e tratamento de erros |
| ART-066 | [Regras e Orientacao para Upload de Planilhas](https://intercom.help/compliasset/pt-BR/articles/11830342-regras-e-orientacao-para-upload-de-planilhas) | Regras gerais de importacao de Colaboradores, Fundos, Investidores e Terceiros | Vigente a confirmar | 2026-09-10 | Publicado em 25/07/2025; confirmar limites, identificadores, validacao bloqueante, reativacao e inconsistencia do limite de Investidores |
| ART-067 | [7 Funcionalidades Coringas na Secao de Relacionados](https://intercom.help/compliasset/pt-BR/articles/15350862-7-funcionalidades-coringas-na-secao-de-relacionados) | Atalhos, acessos, evidencias, Eventos e Due Diligence em Relacionados | Vigente a confirmar | 2026-09-10 | Publicado em 03/06/2026; confirmar permissoes, transferencia de demandas, escopo de visibilidade, auditoria e ciclos de DDQ |
| ART-068 | [Upload de Novos Colaboradores](https://intercom.help/compliasset/pt-BR/articles/5520614-upload-de-novos-colaboradores) | Importacao, atualizacao e reativacao de Colaboradores por CSV | Vigente a confirmar | 2026-09-10 | Publicado em 26/04/2024; confirmar modelo, estados da pre-visualizacao, envio unico de boas-vindas, limite e regras de atualizacao |
| ART-069 | [Atribuicoes do Perfil Colaborador](https://intercom.help/compliasset/pt-BR/articles/7183438-atribuicoes-do-perfil-colaborador) | Visao de Colaborador, demandas, evidencias e permissoes | Vigente a confirmar | 2026-09-10 | Publicado em 20/05/2026; confirmar secoes, cartoes, acoes permitidas, certificados, exportacao de respostas e isolamento de acesso |
| ART-070 | [Alteracao de Colaborador para Membro](https://intercom.help/compliasset/pt-BR/articles/7153535-alteracao-de-colaborador-para-membro) | Promocao de Colaborador, perfis de Membro e acessos por secao | Vigente a confirmar | 2026-09-10 | Publicado em 24/10/2024; confirmar pre-condicoes, menor privilegio, areas configuraveis, permissao administrativa e efeitos em sessoes |
| ART-071 | [Compartilhar Fundos, Investidores e Terceiros com Colaboradores](https://intercom.help/compliasset/pt-BR/articles/5596387-compartilhar-fundos-investidores-e-terceiros-com-colaboradores) | Permissao pontual de acesso a perfis de Relacionados | Vigente a confirmar | 2026-09-10 | Publicado em 20/09/2024; confirmar prazos, notificacoes, permissoes de comentario e anexo, revogacao e isolamento de acesso |
| ART-072 | [Categorizar Colaboradores em Funcoes](https://intercom.help/compliasset/pt-BR/articles/4636444-categorizar-colaboradores-em-funcoes) | Funcoes, classificacao e associacao de Colaboradores | Vigente a confirmar | 2026-09-10 | Publicado em 23/05/2025; confirmar permissoes, associacoes multiplas, duplicidade, exclusao e impactos em filtros e campanhas |
| ART-073 | [Investimentos Pessoais de Colaboradores](https://intercom.help/compliasset/pt-BR/articles/4951125-investimentos-pessoais-de-colaboradores) | Canal de Compliance, aprovacao e Eventos de investimentos pessoais | Vigente a confirmar | 2026-09-10 | Publicado em 24/10/2024; confirmar destinatarios, natureza, status, decisao, notificacoes, permissoes e retencao de dados |
| ART-074 | [Editar 'Atalhos' na Visao de Colaborador](https://intercom.help/compliasset/pt-BR/articles/4561615-editar-atalhos-na-visao-de-colaborador) | Naturezas de Eventos, Atalhos e Reportes de Compliance | Vigente a confirmar | 2026-09-10 | Publicado em 05/12/2024; confirmar permissao administrativa, dependencia entre colunas, natureza, confirmacao, reportes e efeitos em Eventos existentes |
| ART-075 | [Desativar Acesso de Colaborador](https://intercom.help/compliasset/pt-BR/articles/4582671-desativar-acesso-de-colaborador) | Desligamento, bloqueio de acesso e transferencia de responsabilidades | Vigente a confirmar | 2026-09-10 | Publicado em 22/11/2024; confirmar datas, momento da transferencia, status elegiveis, permissao, sessoes, auditoria e retencao |
| ART-076 | [Retornar Acesso de Ex-Colaborador](https://intercom.help/compliasset/pt-BR/articles/8733090-retornar-acesso-de-ex-colaborador) | Reativacao de Ex-Colaborador por perfil ou planilha | Vigente a confirmar | 2026-09-10 | Publicado em 19/08/2024; confirmar limpeza da Data de Demissao, login preservado, reativacao em massa, permissao e tratamento de excluidos |
| ART-077 | [Mandatos de Colaboradores](https://intercom.help/compliasset/pt-BR/articles/9516488-mandatos-de-colaboradores) | Mandatos, poderes de atuacao e historico de Colaboradores | Vigente a confirmar | 2026-09-10 | Publicado em 22/08/2024; confirmar campos, permissoes, vigencias, multiplos mandatos, exclusao e auditoria no Historico |
| ART-078 | [Certificacoes de Colaboradores](https://intercom.help/compliasset/pt-BR/articles/9761125-certificacoes-de-colaboradores) | Certificacoes, pontuacao PEC, anexos e alertas de vencimento | Vigente a confirmar | 2026-09-10 | Publicado em 16/06/2026; confirmar campos, periodos, pontuacao, permissoes, anexos, notificacoes e auditoria |
| ART-079 | [Atualizacao de Colaboradores](https://intercom.help/compliasset/pt-BR/articles/15001248-atualizacao-de-colaboradores) | Atualizacao em massa de Colaboradores por planilha | Vigente a confirmar | 2026-09-10 | Publicado em 07/05/2026; confirmar campos identificadores, campos atualizaveis, reativacao por e-mail, limite, permissoes, erros e auditoria |
| ART-080 | [Exclusao de Colaboradores](https://intercom.help/compliasset/pt-BR/articles/9970843-exclusao-de-colaboradores) | Exclusao, perda de dados de Eventos e recriacao de Colaboradores | Vigente a confirmar | 2026-09-10 | Publicado em 22/11/2024; confirmar pre-requisitos, impactos em dossies, permissoes, recuperacao, retencao e alternativa de desativacao |
| ART-081 | [Upload de Relacionados via Planilha](https://intercom.help/compliasset/pt-BR/articles/4570873-upload-de-relacionados-via-planilha) | Upload de Fundos, Investidores, Terceiros e Colaboradores por modelos especificos | Vigente a confirmar | 2026-09-10 | Publicado em 15/08/2023; confirmar modelos, campos, identificadores, limites, permissoes, erros e fontes especificas por tipo de Relacionado |
| ART-082 | [Realizando DD Inicial e Periodica de Terceiros](https://intercom.help/compliasset/pt-BR/articles/7170567-realizando-dd-inicial-e-periodica-de-terceiros) | Due Diligence inicial, revisao periodica, DDQ e Background Check de Terceiros | Vigente a confirmar | 2026-09-10 | Publicado em 29/04/2026; confirmar situacoes, questionarios, prazos, cobrancas, documentos, riscos, periodicidade, permissoes e custos do Data Engine |
| ART-083 | [Prorrogacao de Prazos em Due Diligence](https://intercom.help/compliasset/pt-BR/articles/4360593-prorrogacao-de-prazos-em-due-diligence) | Alteracao do prazo de resolucao de Eventos de Due Diligence | Vigente a confirmar | 2026-09-10 | Publicado em 05/12/2024; confirmar permissao, dias corridos, prazos vencidos, cobrancas, notificacoes, auditoria e efeitos em DDQ inicial e periodica |
| ART-084 | [Upload de Novos Investidores](https://intercom.help/compliasset/pt-BR/articles/7919004-upload-de-novos-investidores) | Importacao em massa de Investidores por CSV | Vigente a confirmar | 2026-09-10 | Publicado em 05/07/2023; confirmar modelo, campos obrigatorios, codigos de pessoa e risco, limites, simulacao, identificacao e processamento |
| ART-085 | [Cadastro de Investidores](https://intercom.help/compliasset/pt-BR/articles/4360283-cadastro-de-investidores) | Cadastro, perfil, status, Eventos e Dossie Reputacional de Investidores | Vigente a confirmar | 2026-09-10 | Publicado em 30/09/2025; confirmar campos por tipo, datas, Grupos, Ativos/Inativos, permissoes, exportacao, auditoria e exclusao |
| ART-086 | [Cadastro de Fundos](https://intercom.help/compliasset/pt-BR/articles/4582372-cadastro-de-fundos) | Cadastro, grupos, status e exportacao de Fundos | Vigente a confirmar | 2026-09-10 | Publicado em 06/10/2025; confirmar campos obrigatorios, risco, datas, gestores, Grupos, Desativados, filtros, permissoes e exportacao |
| ART-087 | [Upload de Novos Fundos](https://intercom.help/compliasset/pt-BR/articles/7903584-upload-de-novos-fundos) | Importacao em massa de Fundos por CSV | Vigente a confirmar | 2026-09-10 | Publicado em 14/08/2023; confirmar modelo, campos, CSV, simulacao, identificacao, limites, processamento e auditoria |
| ART-088 | [Reenvio de Due Diligence para Terceiros](https://intercom.help/compliasset/pt-BR/articles/12961469-reenvio-de-due-diligence-para-terceiros) | Reenvio de lembrete, prazo e historico de Due Diligence | Vigente a confirmar | 2026-09-10 | Publicado em 28/11/2025; confirmar permissoes, limites de reenvio, entrega, cobrancas, protecao contra abuso e Historico |
| ART-089 | [Upload de Novos Terceiros](https://intercom.help/compliasset/pt-BR/articles/8260556-upload-de-novos-terceiros) | Importacao em massa de Terceiros por CSV | Vigente a confirmar | 2026-09-10 | Publicado em 15/08/2023; confirmar campos obrigatorios, documentos, codigos, simulacao, limites, identificacao e efeitos em DDQ |
| ART-090 | [Cadastro de Terceiros](https://intercom.help/compliasset/pt-BR/articles/8257454-cadastro-de-terceiros) | Cadastro, categorias, grupos e perfil de Terceiros | Vigente a confirmar | 2026-09-10 | Publicado em 30/09/2025; confirmar campos por tipo, CNPJ alfanumerico, categorias, Grupos, permissoes, DD e Dossie Reputacional |
| ART-091 | [Diferenca entre Dossie Reputacional e Due Diligence de Terceiros](https://intercom.help/compliasset/pt-BR/articles/8429615-diferenca-entre-dossie-reputacional-e-due-diligence-de-terceiros) | Diferenciacao entre consulta reputacional e Due Diligence | Vigente a confirmar | 2026-09-10 | Publicado em 29/04/2026; confirmar custos, escopo, questionarios, documentos, risco, permissoes, privacidade e retencao |

Atualize esta base quando uma regra documentada, fonte ou contexto permanente mudar. Registre regras especificas de produto nos documentos do respectivo modulo e mantenha neste arquivo apenas o contexto necessario para orientar novas demandas. Mantenha o processo de trabalho de PM e PO no [guia operacional de abertura de cards](guia_abertura_cards_pm_po.md).
