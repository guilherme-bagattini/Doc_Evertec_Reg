# Guia para abrir cards e demandas do CompliAsset

## Finalidade

Este documento deve ser consultado sempre que uma nova demanda, melhoria, bug, duvida funcional ou necessidade de investigacao for transformada em card.

O objetivo e garantir que a demanda:

- esteja ligada ao funcionamento real do CompliAsset e do EvertecReg;
- descreva um problema ou resultado esperado, e nao apenas uma ideia solta;
- tenha contexto suficiente para produto, design, desenvolvimento e validacao;
- seja rastreavel ate a fonte da necessidade;
- possa ser priorizada e testada.

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

Ao analisar uma demanda, considere sempre tres perguntas:

1. O que precisa ser interpretado do ponto de vista regulatorio?
2. O que precisa virar tarefa, decisao ou acao operacional?
3. O que precisa ser registrado para gerar evidencia, historico e auditoria?

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

## Regras de seguranca ja confirmadas

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

| ID | Material | Assunto | Status | Data de consulta | Observacao |
|---|---|---|---|---|---|
| ART-001 | [Alteracao de Nomes e E-mails de Colaboradores](https://intercom.help/compliasset/pt-BR/articles/4789039-alteracao-de-nomes-e-e-mails-de-colaboradores) | Seguranca e cadastro de colaboradores | Vigente a confirmar | 2026-09-02 | Publicado em 26/04/2023; regra de alteracao de nome requer confirmacao |
| ART-002 | [Autenticacao de Dois Fatores](https://intercom.help/compliasset/pt-BR/articles/1956042-autenticacao-de-dois-fatores) | Seguranca e acesso | Vigente a confirmar | 2026-09-02 | Publicado em 02/05/2023; confirmar se o fluxo atual permanece igual |

Atualize este guia quando uma regra permanente de abertura de cards mudar. Registre regras especificas de produto nos documentos do respectivo modulo e mantenha neste arquivo apenas o contexto necessario para orientar novas demandas.
