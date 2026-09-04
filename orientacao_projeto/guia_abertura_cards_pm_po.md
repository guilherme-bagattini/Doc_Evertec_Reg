# Guia de definicao e abertura de cards: PM e PO

## Finalidade

Este guia define como transformar uma necessidade em um card claro, priorizavel e executavel, e como dividir as responsabilidades entre Product Manager (PM), Product Owner (PO), desenvolvimento, design e validacao.

Use este documento para conduzir o trabalho de abertura e refinamento. Use a [Base de conhecimento do CompliAsset](base_conhecimento_compliasset.md) para consultar contexto funcional, regras documentadas, fontes e o template detalhado de card.

As responsabilidades abaixo sao uma referencia de trabalho. A decisao final deve respeitar a estrutura, os papeis e os acordos vigentes do time.

## Como este guia se relaciona com a base

Os dois documentos cumprem funcoes diferentes e complementares:

| Documento | Funcao principal | Deve responder |
|---|---|---|
| [Base de conhecimento do CompliAsset](base_conhecimento_compliasset.md) | Contexto funcional, regras documentadas e fontes | O que sabemos sobre o produto e como essa informacao foi comprovada? |
| Este guia | Processo de PM/PO e estrutura de trabalho | Como transformar o contexto em uma decisao, investigacao ou card executavel? |
| Card ou documento de decisao | Registro da demanda e do resultado | O que foi decidido, por que, por quem e como sera validado? |

### Fluxo de consulta

1. Comece neste guia para classificar a demanda e escolher entre Brief, discovery, investigacao ou implementacao.
2. Consulte a [base de conhecimento](base_conhecimento_compliasset.md) para verificar regras, modulos, fontes, permissoes e comportamentos documentados.
3. Retorne a este guia para preencher o Product Brief, a matriz CSD, a priorizacao e o card.
4. Vincule no card as fontes da base e registre como pendente tudo que ainda nao foi confirmado.

A base fornece evidencia e contexto; este guia fornece o metodo de trabalho. Nenhum dos dois substitui a validacao da versao atual do sistema ou uma decisao formal de produto.

## Principios

- Card nasce de um problema, risco, oportunidade ou obrigacao, e nao de uma solucao presumida.
- Fato observado, necessidade do usuario, hipotese e decisao confirmada devem estar separados.
- Um card deve representar uma unidade de valor que possa ser entendida, desenvolvida e validada.
- Criterios de aceite descrevem comportamento verificavel; nao sao uma lista de tarefas tecnicas.
- Duvidas relevantes ficam registradas no card ou vinculadas a uma demanda de investigacao.
- Permissoes, auditoria, historico, dados, integracoes, notificacoes e privacidade entram na analise desde o inicio.

## Antes do card: Product Brief

O Product Brief e a sintese do contexto, da direcao e do resultado esperado de uma iniciativa. Ele evita que o time comece discutindo uma solucao sem entender o problema que precisa ser resolvido.

Nem toda demanda precisa de um Brief extenso. Para um bug simples, o contexto pode caber no proprio card. Para uma iniciativa nova, uma mudanca transversal ou uma demanda com muitas partes interessadas, registre o Brief antes de decompor o trabalho em cards.

### Perguntas essenciais

- Qual e a demanda e em que contexto ela surgiu?
- Qual objetivo de negocio ou iniciativa esta sendo apoiado?
- Qual produto, modulo ou fluxo sera impactado?
- Por que isso e importante agora?
- Qual problema, risco ou oportunidade estamos tratando?
- Quem sao os usuarios, clientes, areas ou partes interessadas afetados?
- Como saberemos que tivemos sucesso?
- Quais metas podem ser mensuradas e quais sinais qualitativos importam?
- Existem limitacoes, requisitos ou desejos de design?
- Que pesquisas, entrevistas, documentos, dinamicas ou cards relacionados ja existem?

O Brief deve registrar respostas conhecidas e marcar como pendentes as que ainda precisam de investigacao. Ele orienta o trabalho, mas nao substitui criterios de aceite nem uma decisao de escopo.

### Template de Product Brief

```markdown
# Product Brief: [nome da iniciativa]

## Contexto
- Qual demanda iniciou esta iniciativa?
- Em que situacao ela surgiu?
- Qual objetivo de negocio ou iniciativa ela apoia?

## Problema ou oportunidade
- O que precisa ser resolvido ou explorado?
- Quem e afetado?
- Qual e o impacto atual?

## Por que agora
- Qual e a urgencia, risco, prazo ou dependencia?
- O que acontece se nada for feito?

## Produto e escopo inicial
- Produto, modulo ou fluxo impactado:
- O que parece estar incluido:
- O que esta explicitamente fora do escopo:

## Sucesso
- Resultado esperado:
- Indicadores ou metas:
- Sinais qualitativos:

## Restricoes e referencias
- Limitacoes de negocio, design, tecnologia ou regulacao:
- Usuarios, clientes e stakeholders:
- Pesquisas, entrevistas, documentos ou cards relacionados:

## Responsaveis
- PM:
- PO:
- Outras pessoas ou areas:
```

## Planning: organizar a descoberta e a execucao

Planning e o planejamento interno necessario para transformar o contexto em um caminho de trabalho. O plano depende do tipo de demanda, mas normalmente deve:

1. consolidar o Product Brief;
2. identificar o problema ou oportunidade inicial;
3. definir objetivos ou resultados esperados;
4. escolher a abordagem adequada, como analise de dados, entrevista, teste de usabilidade, prototipo, avaliacao tecnica ou entrega incremental;
5. mapear certezas, suposicoes e duvidas;
6. definir quais evidencias serao necessarias para tomar a proxima decisao;
7. decompor a iniciativa em investigacoes, decisoes e cards de implementacao.

O Planning nao deve ser usado para criar etapas por formalidade. Cada etapa precisa responder a uma incerteza, gerar uma decisao ou produzir uma entrega verificavel.

### Gate de decisao

Antes de criar um card de implementacao, escolha o proximo passo com base no nivel de clareza:

| Situacao | Proximo passo |
|---|---|
| Problema compreendido e solucao suficientemente definida | Card de implementacao |
| Problema compreendido, mas solucao incerta | Card de investigacao ou discovery |
| Problema ainda incerto | Entrevista, analise de dados ou outra pesquisa |
| Demanda sem contexto, valor ou responsavel suficiente | Devolver para complementacao |

O gate nao e uma etapa burocratica. Ele evita que uma hipotese de solucao seja registrada como requisito e que o time comece a desenvolver antes de conhecer o problema.

### Matriz CSD

A matriz CSD organiza o conhecimento do time em tres grupos:

| Grupo | O que registrar | Proximo movimento |
|---|---|---|
| Certezas | Fatos confirmados, regras vigentes, dados observados e decisoes registradas | Confirmar a fonte e usar como restricao ou contexto |
| Suposicoes | Hipoteses, interpretacoes e afirmacoes ainda nao comprovadas | Definir como validar ou rebaixar a confianca |
| Duvidas | O que o time ainda nao sabe e precisa descobrir | Transformar em pergunta, investigacao ou decisao |

A matriz e viva. Uma duvida pode virar certeza, uma suposicao pode ser descartada e novas duvidas podem surgir. Registre a evidencia e a data da mudanca; nao mova um item para `Certezas` apenas porque houve consenso informal.

No card, use a matriz para separar `Fatos confirmados`, `Hipoteses a validar` e `Duvidas ou dependencias`. Quando uma suposicao mudar o escopo, o risco ou o criterio de aceite, abra uma investigacao antes de marcar o card como pronto para desenvolvimento.

### Modelo copiavel de CSD

```markdown
## Matriz CSD

### Certezas
- Fato ou regra:
	- Fonte ou evidencia:
	- Data da confirmacao:

### Suposicoes
- Hipotese:
	- Como validar:
	- Responsavel:
	- Prazo:

### Duvidas
- Pergunta:
	- Evidencia necessaria:
	- Proximo passo:
	- Responsavel:
```

## Controle de vieses na descoberta

Decisoes de produto podem ser distorcidas pela forma como o time escolhe evidencias e interpreta relatos. Antes de priorizar ou definir uma solucao, faça perguntas que desafiem a primeira leitura.

- **Vies de sobrevivencia:** nao pesquise somente clientes ativos e satisfeitos; inclua quem abandonou, nao adotou ou teve dificuldade.
- **Vies de afinidade:** nao valide uma ideia apenas com pessoas parecidas com o time; busque perfis, contextos e niveis de experiencia diferentes.
- **Efeito da opiniao mais influente:** registre evidencias individualmente antes da discussao para que autoridade ou senioridade nao substitua dados.
- **Ancoragem na primeira solucao:** escreva o problema e os resultados antes de escolher tecnologia, tela ou fluxo.
- **Confirmacao:** procure deliberadamente evidencias que contradigam a hipotese, e nao apenas sinais que a apoiem.

Isso nao elimina vieses, mas torna suas fontes visiveis e reduz o risco de transformar uma amostra limitada em regra de produto. Registre no Planning quem foi ouvido, quem ficou de fora e quais limitacoes a pesquisa teve.

## Papeis e responsabilidades

### PM: direcao do produto

O PM e responsavel por conectar a demanda aos objetivos do produto e do negocio. Em geral, deve:

- identificar o problema, publico afetado e resultado de negocio esperado;
- avaliar oportunidade, risco, urgencia, impacto regulatorio e dependencias;
- alinhar contexto com clientes, negocio e demais partes interessadas;
- decidir ou propor prioridade com base em valor, risco, esforco e estrategia;
- garantir que a demanda tenha uma pergunta de produto clara antes de entrar no backlog;
- comunicar o que esta dentro e fora do escopo da iniciativa.

O PM nao deve substituir a validacao tecnica, escrever requisitos de implementacao sem apoio do time ou tratar pedido de stakeholder como prioridade automatica.

### PO: clareza e prontidao para execucao

O PO e responsavel por transformar a direcao do produto em trabalho compreensivel e ordenado para o time. Em geral, deve:

- detalhar fluxo, regras, perfis, estados, excecoes e resultado esperado;
- manter o card pequeno o suficiente para ser desenvolvido e validado;
- esclarecer dependencias, dados necessarios e perguntas em aberto;
- ordenar o backlog e preparar os itens para refinamento e planejamento;
- conduzir o alinhamento com design, desenvolvimento, QA e partes interessadas;
- validar se a entrega atende aos criterios de aceite e ao problema original;
- atualizar o card quando uma decisao mudar seu escopo ou comportamento.

O PO nao deve inventar regra de negocio para preencher lacunas, aprovar sozinho uma mudanca de escopo relevante ou usar criterio subjetivo como aceite.

### Responsabilidades compartilhadas

PM e PO devem trabalhar juntos para:

- confirmar quem e o usuario ou area afetada;
- separar necessidade de solucao;
- identificar riscos e impacto de nao fazer;
- decidir se o proximo passo e implementar, investigar, corrigir ou apenas documentar;
- registrar decisoes e fontes de evidencia;
- garantir que a entrega tenha uma forma objetiva de ser validada.

### Visao rapida por responsabilidade

| Tema | PM | PO |
|---|---|---|
| Problema e estrategia | Responsavel | Contribui |
| Priorizacao | Decide ou recomenda | Organiza o backlog |
| Regras e fluxo | Orienta | Detalha |
| Criterios de aceite | Valida o resultado | Especifica e acompanha |
| Discovery | Define perguntas | Organiza evidencias |
| Execucao | Acompanha valor | Acompanha entrega |

## Quando abrir um card

Abra um card quando houver uma unidade de trabalho rastreavel, como:

- **Bug:** comportamento que viola uma regra, expectativa ou criterio existente.
- **Melhoria:** mudanca que aumenta valor, eficiencia, clareza ou controle de um fluxo.
- **Nova capacidade:** funcionalidade ou fluxo ainda inexistente.
- **Investigacao:** incerteza que precisa de evidencia, prototipo, analise tecnica ou validacao com usuario.
- **Divida ou decisao:** ponto que exige alinhamento formal antes de implementar.
- **Obrigacao regulatoria:** necessidade com fonte, prazo, impacto e evidencia esperada.
- **Tarefa tecnica:** trabalho interno necessario para sustentar o produto, com resultado verificavel.

Nao abra um card separado para cada subtarefa tecnica quando elas fazem parte da mesma entrega. Separe cards quando houver valor, responsavel, criterio de aceite ou ciclo de validacao independente.

## Como priorizar

A prioridade deve ter uma justificativa registrada, e nao depender apenas da ordem de chegada ou da pessoa que solicitou a demanda. Considere:

- impacto para clientes, usuarios e operacao;
- urgencia, prazo externo e custo de atraso;
- risco regulatorio, financeiro, operacional ou de seguranca;
- quantidade e criticidade das pessoas afetadas;
- dependencias e desbloqueios para outras entregas;
- esforco estimado e complexidade;
- confianca nas evidencias disponiveis;
- alinhamento com os objetivos do produto e do MVP.

Uma demanda de alto impacto, mas baixa confianca sobre o problema, pode precisar de discovery antes de receber prioridade de implementacao. Registre a decisao, quem participou e quais fatores pesaram.

## Fluxo recomendado

1. **Capturar:** registrar a demanda bruta, origem, data, solicitante e evidencias.
2. **Contextualizar:** preencher o Product Brief na medida adequada ao tamanho e ao risco da iniciativa.
3. **Classificar:** definir tipo de card, modulo, fluxo afetado e se e problema, oportunidade, risco ou obrigacao.
4. **Planejar:** organizar o CSD, escolher a investigacao necessaria e definir a evidencia para a proxima decisao.
5. **Investigar:** consultar a base de conhecimento, reproduzir o comportamento e separar fatos de hipoteses.
6. **Definir:** escrever problema, resultado esperado, escopo, regras, impactos e criterios de aceite.
7. **Priorizar:** avaliar valor, urgencia, risco, dependencia, esforco e custo de atraso.
8. **Refinar:** revisar com PM, PO, design, desenvolvimento e validacao; dividir ou complementar o card quando necessario.
9. **Planejar a entrega:** ordenar no backlog e confirmar que o time consegue iniciar sem depender de informacao essencial ausente.
10. **Executar:** acompanhar decisoes, bloqueios, mudancas de escopo e evidencias durante o desenvolvimento.
11. **Validar:** conferir criterios de aceite, cenarios de erro, permissoes, dados, historico e impacto no fluxo existente.
12. **Encerrar:** registrar resultado, evidencias, pendencias residuais e links para entrega, decisao ou documentacao.

## Definicao de pronto para desenvolvimento

Um card esta pronto para entrar no planejamento quando:

- o problema e o usuario afetado estao claros;
- o tipo, modulo e origem da demanda foram registrados;
- o resultado esperado pode ser descrito sem depender de uma conversa oral;
- o escopo inclui e nao inclui esta delimitado;
- regras de negocio, perfis e estados conhecidos estao documentados;
- criterios de aceite sao objetivos e testaveis;
- dependencias, riscos e perguntas em aberto estao explicitos;
- design, desenvolvimento e validacao sabem o que precisam analisar;
- a prioridade foi discutida e o motivo esta registrado;
- nao existe bloqueio de informacao essencial para iniciar o trabalho.

Um card pode ser priorizado para investigacao mesmo sem estar pronto para desenvolvimento. Nesse caso, o resultado esperado deve ser uma decisao, evidencia ou recomendacao, e nao uma implementacao presumida.

## Definicao de pronto para encerramento

Antes de encerrar, confirme que:

- os criterios de aceite foram validados;
- o comportamento atual e o novo foram comparados quando aplicavel;
- permissoes e perfis foram testados;
- dados, historico, auditoria e integracoes foram considerados;
- cenarios de erro, vazio, atraso e duplicidade foram avaliados quando aplicavel;
- as evidencias de validacao foram anexadas ou vinculadas;
- documentacao, decisao ou base de conhecimento foi atualizada quando necessario;
- pendencias conhecidas nao foram ocultadas e possuem destino definido.

## Exemplos no contexto do EvertecReg

### Nova fonte regulatoria

- **Product Brief:** entender qual fonte precisa ser acompanhada, qual cliente ou modulo e afetado e qual risco existe se a informacao nao for capturada.
- **Planning:** validar acesso, formato, frequencia, qualidade do conteudo e criterio de relevancia antes de transformar a necessidade em implementacao.
- **Cards possiveis:** investigacao da fonte, regra de filtragem, captura, analise de impacto, distribuicao e auditoria.

### Falha na distribuicao para Jira ou Teams

- **Problema:** uma informacao aprovada nao chega ao canal esperado ou chega sem dados necessarios.
- **Evidencias:** identificador da execucao, ambiente, horario, status exibido, log correlato e destino esperado. Nao incluir credenciais ou dados sensiveis.
- **Criterios de aceite:** confirmar sucesso, falha, retentativa, mensagem para o usuario, detalhe no log e preservacao da trilha de auditoria.

### Status generico na interface

- **Problema:** o usuario ve uma falha sem conseguir entender o proximo passo.
- **Discovery:** separar o que precisa ser compreendido pelo usuario do diagnostico que deve permanecer nos logs.
- **Resultado:** mensagem acionavel na interface, identificador para suporte e log detalhado para diagnostico, sem expor informacao sensivel.

Os exemplos sao ilustrativos. As regras vigentes devem ser confirmadas nas decisoes do MVP, na base de conhecimento e com as areas responsaveis.

## Modelo de card

```markdown
# [TIPO] Titulo orientado ao resultado

## Contexto e origem
- Solicitante:
- Cliente, area ou usuario afetado:
- Modulo ou fluxo:
- Fonte, evidencia ou card relacionado:
- Data:

## Problema ou oportunidade
Descreva o que acontece, quem e afetado e qual e o impacto.

## Resultado esperado
Descreva o comportamento ou resultado que deve ser possivel observar.

## Escopo
### Inclui
- 

### Nao inclui
- 

## Regras e cenarios
- Regra principal:
- Permissoes e perfis:
- Cenario de sucesso:
- Cenarios de erro, vazio ou excecao:
- Dados, historico e auditoria:
- Integracoes, notificacoes e prazos:

## Criterios de aceite
- [ ] 
- [ ] 
- [ ] 

## Dependencias e duvidas
- 

## Evidencias de validacao
- 

## Decisoes registradas
- 
```

## Checklist rapido do PM

- [ ] O contexto e o objetivo da iniciativa foram registrados em um Product Brief proporcional ao problema?
- [ ] O card resolve um problema relevante ou atende uma obrigacao clara?
- [ ] O usuario, cliente ou area afetada foi identificado?
- [ ] O impacto de nao fazer esta descrito?
- [ ] A prioridade tem justificativa?
- [ ] O escopo esta coerente com o objetivo?
- [ ] A demanda depende de uma investigacao antes da implementacao?
- [ ] A pesquisa considera usuarios ativos, inativos, novos e diferentes perfis quando aplicavel?

## Checklist rapido do PO

- [ ] Certezas, suposicoes e duvidas estao separadas?
- [ ] O fluxo atual e o comportamento esperado estao descritos?
- [ ] Fatos, hipoteses e decisoes foram separados?
- [ ] As regras, perfis, estados e excecoes estao claras?
- [ ] Os criterios de aceite podem ser testados objetivamente?
- [ ] As dependencias e duvidas estao visiveis?
- [ ] O time consegue iniciar sem depender de conhecimento oral?
- [ ] A validacao e as evidencias de conclusao foram previstas?

## O que evitar

- Abrir um card apenas com “ajustar tela”, “melhorar fluxo” ou “corrigir integracao”, sem problema e resultado esperado.
- Transformar automaticamente um pedido de stakeholder em requisito ou prioridade.
- Misturar problema, investigacao e implementacao no mesmo card sem indicar a etapa atual.
- Registrar uma hipotese como regra confirmada.
- Escrever “melhorar performance” sem indicar medida, cenario ou resultado observavel.
- Repetir subtarefas tecnicas em cards separados quando elas pertencem a uma mesma entrega.
- Encerrar o card sem evidencia de validacao ou sem destino para pendencias conhecidas.

## Relacao com a base de conhecimento

Consulte a base antes de escrever uma regra de produto. Registre no card o artigo, documento, entrevista, log, ambiente ou validacao que sustenta a informacao. Quando houver contradicao ou informacao desatualizada, crie ou vincule uma investigacao e mantenha a regra como pendente de confirmacao.

A [base de conhecimento](base_conhecimento_compliasset.md) concentra contexto do CompliAsset e materiais de referencia. Este guia concentra o processo de trabalho de PM e PO. Regras especificas de um modulo devem permanecer documentadas no material do proprio modulo ou na fonte oficial correspondente; o card deve vincular as duas coisas quando a demanda depender de uma regra do produto.
