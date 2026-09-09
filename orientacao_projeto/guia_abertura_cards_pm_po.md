# Guia de definicao e abertura de cards: PM e PO

## Finalidade

Este guia define como transformar uma necessidade em um card claro, priorizavel e executavel, e como dividir as responsabilidades entre Product Manager (PM), Product Owner (PO), desenvolvimento, design e validacao.

Use este documento para conduzir o trabalho de abertura e refinamento. Use a [Base de conhecimento do CompliAsset](base_conhecimento_compliasset.md) para consultar contexto funcional, regras documentadas e fontes. O modelo operacional de card deste guia deve ser usado para registrar a demanda.

As responsabilidades abaixo sao uma referencia de trabalho. A decisao final deve respeitar a estrutura, os papeis e os acordos vigentes do time.

## Resumo para o dia a dia

Use este guia como uma sequencia de perguntas praticas:

1. **Qual problema estamos tentando resolver?** Descreva o usuario afetado, o contexto e o impacto antes de falar da solucao.
2. **O que sabemos e como sabemos?** Separe fatos confirmados, hipoteses e duvidas. Vincule a fonte ou evidencia.
3. **Qual e o proximo passo correto?** Decida entre investigar, decidir, corrigir, melhorar ou implementar.
4. **Como saberemos que funcionou?** Defina resultado esperado, criterios de aceite e evidencia de validacao.
5. **Quem precisa participar?** Envolva PM, PO, desenvolvimento, design, validacao e areas afetadas na medida do risco.

### Regras de bolso

- Nao transforme pedido em requisito sem entender o problema, o impacto e o usuario afetado.
- Nao transforme consenso informal em regra de negocio; registre a fonte, a decisao e a data.
- Se a incerteza puder mudar o escopo, a prioridade ou o criterio de aceite, investigue antes de implementar.
- Um card deve ter um resultado principal, um responsavel claro e uma forma objetiva de validacao.
- Toda demanda deve declarar se pertence ao MVP, a um incremento posterior ou se ainda esta pendente de validacao de escopo.
- Prioridade nao e ordem de chegada: considere valor, risco, urgencia, custo de atraso, dependencia, esforco e confianca.
- O PM protege direcao, contexto e resultado; o PO protege clareza, ordem do backlog e prontidao para execucao.
- Desenvolvimento participa da descoberta e estima o trabalho; nao deve receber uma solucao tecnica fechada sem discutir alternativas.
- Toda mudanca relevante de escopo deve deixar registro no card ou em uma decisao vinculada.
- Nao encerre um card apenas porque foi desenvolvido: confirme comportamento, cenarios de erro, permissoes e evidencia.
- Quando houver conflito entre documento, sistema e relato, trate como investigacao pendente ate a fonte correta ser confirmada.

### Rotina minima recomendada

- **Antes do refinamento:** revisar contexto, problema, escopo, riscos, dependencias e perguntas abertas.
- **Durante o refinamento:** alinhar comportamento, excecoes, impacto tecnico, criterios de aceite e estrategia de validacao.
- **Durante a execucao:** registrar bloqueios, decisoes e mudancas; evitar que informacoes importantes fiquem apenas em reunioes.
- **Antes de concluir:** validar o resultado no fluxo real ou em ambiente apropriado e anexar evidencia.
- **Depois da entrega:** observar o resultado esperado, registrar aprendizados e atualizar a base quando uma regra tiver sido confirmada.

### Estados e passagem de responsabilidade

Use os estados abaixo como referencia. Os nomes podem variar conforme a ferramenta, mas o criterio de passagem deve permanecer explicito:

| Estado | Pergunta de controle | Saida esperada |
|---|---|---|
| Entrada | A demanda tem origem, contexto e responsavel? | Classificacao inicial ou pedido de complementacao |
| Discovery ou investigacao | A principal incerteza esta identificada? | Evidencia, decisao ou recomendacao |
| Pronto para desenvolvimento | O time consegue iniciar sem depender de conhecimento oral? | Card refinado, priorizado e com criterios de aceite |
| Em desenvolvimento | O escopo e as decisoes continuam visiveis? | Entrega candidata a validacao |
| Em validacao | O comportamento foi conferido nos cenarios relevantes? | Aceite, rejeicao fundamentada ou retorno para ajuste |
| Encerrado | O resultado e as pendencias foram registrados? | Evidencia final e documentacao atualizada quando necessario |

Nao avance um card apenas para limpar uma fila. Se o criterio de saida nao foi atendido, registre o bloqueio, a proxima acao e o responsavel.

### Prioridade, urgencia e severidade

Esses conceitos nao sao sinonimos:

- **Prioridade:** ordem de trabalho considerando valor, risco, estrategia e custo de atraso.
- **Urgencia:** quanto tempo existe antes que o impacto aumente ou uma janela seja perdida.
- **Severidade:** tamanho do dano ou alcance do problema, especialmente em bugs.

Um bug pode ser severo, mas ter uma alternativa temporaria e prioridade menor que uma obrigacao com prazo. Da mesma forma, uma demanda urgente pode precisar primeiro de investigacao para evitar uma correcao errada. Registre a justificativa, a data da avaliacao e quem participou da decisao.

### Registro minimo de decisao

Sempre que uma decisao alterar escopo, prioridade, regra ou criterio de aceite, registre:

```markdown
## Decisao - [data]
- Decisao:
- Motivo:
- Evidencias consideradas:
- Alternativas descartadas:
- Impacto no escopo ou prioridade:
- Responsavel pela decisao:
- Proxima revisao, se aplicavel:
```

Uma conversa pode iniciar a decisao, mas o card ou documento vinculado deve ser a fonte consultavel depois.

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

## Escopo do MVP e autoridade de decisao

Antes de priorizar ou abrir um card de implementacao, classifique a demanda em uma destas situacoes:

| Classificacao | Significado | Tratamento |
|---|---|---|
| MVP | Esta prevista nas decisoes fechadas para a primeira etapa | Confirmar aderencia ao fluxo e aos limites definidos em [Decisoes fechadas para o MVP](decisoes_mvp_evertecreg.md) |
| Incremento posterior | Foi explicitamente deixada para uma evolucao futura | Registrar como pos-MVP e nao tratar como compromisso da etapa atual |
| Pendente de validacao | Ha conflito ou falta de evidencia sobre escopo, regra ou capacidade | Abrir investigacao ou decisao antes de prometer implementacao |

As decisoes do MVP sao a referencia para o escopo atual. Quando um card envolver dashboard, alertas, versionamento, permissoes complexas, aprendizagem adaptativa ou outra capacidade listada como posterior, o card deve indicar essa classificacao antes de ser priorizado.

### Autoridade pratica

- **PM:** recomenda ou decide prioridade e enquadramento estrategico, conforme os acordos do time, e confirma se a demanda cabe no objetivo do produto.
- **PO:** organiza o backlog, detalha o comportamento e confirma a prontidao do card; nao encerra sozinho uma regra ainda pendente nem altera o escopo do MVP sem registro.
- **Desenvolvimento e design:** avaliam viabilidade, alternativas, riscos e impacto da solucao; nao devem ser tratados apenas como executores de uma solucao presumida.
- **Stakeholders e areas especialistas:** fornecem contexto, evidencias e restricoes; pedido ou aprovacao de stakeholder nao substitui decisao registrada de produto.
- **Decisao de escopo, regra ou aceite relevante:** deve ter responsavel nomeado no card ou em documento de decisao vinculado.

Quando o projeto nao tiver definido formalmente quem exerce uma dessas autoridades, registre a lacuna em [Duvidas e decisoes em aberto](duvidas_em_aberto_evertecreg.md) antes de usar a regra como definitiva.

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
- Etapa: MVP | Incremento posterior | Pendente de validacao
- O que parece estar incluido:
- O que esta explicitamente fora do escopo:

## Sucesso
- Resultado esperado:
- Indicadores ou metas:
- Sinais qualitativos:

## Eixos do negocio
- Interpretacao regulatoria necessaria:
- Acao operacional esperada:
- Evidencia ou auditoria necessaria:

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

## Frameworks e tecnicas para PM, PO e UX

Frameworks ajudam a estruturar conversas e tornar decisoes comparaveis. Eles nao substituem evidencia, criterio de negocio ou julgamento do time. Use o framework adequado para a pergunta que precisa ser respondida e registre as premissas usadas.

### Como escolher rapidamente

| Pergunta do dia a dia | Framework ou tecnica inicial |
|---|---|
| O que deve ser feito primeiro? | RICE, ICE, WSJF ou Matriz Valor x Esforco |
| O que e essencial para uma entrega? | MoSCoW |
| Qual problema ou necessidade devemos investigar? | Entrevista, JTBD, 5 Porques ou Opportunity Solution Tree |
| Como gerar alternativas sem julgar cedo demais? | Brainstorming ou Crazy 8s |
| Como entender o fluxo atual do usuario? | Jornada do Usuario ou Service Blueprint |
| Como organizar uma experiencia ou escopo? | User Story Mapping |
| Como transformar uma necessidade em comportamento verificavel? | User Story, Gherkin ou criterios de aceite |
| Como avaliar se uma ideia atende diferentes perfis? | Kano |
| Como medir se a experiencia melhorou? | HEART, funil, metricas de produto ou resultado definido no Brief |

### Regras para usar frameworks

- Comece pela pergunta e pelo objetivo; nao escolha um framework apenas porque ele e conhecido.
- Use dados observados e deixe explicitas as estimativas ou opinioes.
- Nao compare pontuacoes feitas com escalas, horizontes ou premissas diferentes sem revisar a base.
- Framework de priorizacao ordena opcoes; nao transforma automaticamente a primeira colocada em compromisso de entrega.
- Quando a confianca for baixa, priorize aprender antes de construir.
- Registre data, participantes, dados utilizados, premissas e resultado no card ou documento de decisao.
- Reavalie a decisao quando surgirem novas evidencias, mudarem os objetivos ou aumentarem os riscos.

### Priorizacao

#### RICE

Indicado para comparar oportunidades ou itens de backlog quando houver estimativas razoaveis de alcance e impacto.

**Formula:** `RICE = Reach x Impact x Confidence / Effort`

- **Reach:** quantas pessoas, clientes ou casos serao afetados no periodo definido.
- **Impact:** quanto o item contribui para o resultado; use uma escala definida pelo time.
- **Confidence:** confianca nas estimativas de alcance e impacto, expressa como percentual.
- **Effort:** esforco estimado pelo time, incluindo produto, design, desenvolvimento e validacao quando aplicavel.

**Como usar:** defina o periodo e as escalas, estime cada fator, registre as fontes e ordene os itens pela pontuacao. Use a pontuacao como apoio a decisao, revisando manualmente riscos regulatorios, dependencias e obrigacoes que a formula nao representa bem.

#### ICE

Indicado para uma comparacao mais rapida, especialmente em discovery, experimentos ou quando o alcance ainda e incerto.

**Formula:** `ICE = Impact x Confidence x Ease`

- **Impact:** potencial de gerar resultado.
- **Confidence:** confianca na avaliacao.
- **Ease:** facilidade relativa de executar ou testar.

**Como usar:** use a mesma escala para todos os itens, descreva o que cada nota significa e prefira testar rapidamente ideias de alta oportunidade e baixo custo. Evite falsa precisao: notas muito detalhadas nao significam estimativas mais confiaveis.

#### MoSCoW

Indicado para definir escopo de uma entrega, release ou MVP junto com stakeholders e time.

- **Must have:** sem isso, o objetivo ou a obrigacao nao pode ser atendido.
- **Should have:** importante, mas existe uma alternativa ou pode ser entregue depois sem inviabilizar o objetivo.
- **Could have:** desejavel, com impacto menor.
- **Won't have now:** explicitamente fora desta entrega ou ciclo.

**Como usar:** comece pelo objetivo da entrega, classifique cada item e valide se o conjunto de `Must have` cabe na capacidade e atende ao resultado. O `Won't have now` deve ser registrado para evitar que itens excluidos retornem como expectativa informal.

#### WSJF

Indicado para ordenar trabalho quando o custo do atraso e a dimensao dos itens precisam ser comparados, especialmente em portflios ou fluxos com muitas dependencias.

**Formula:** `WSJF = Cost of Delay / Job Size`

O custo do atraso pode considerar valor para o usuario ou negocio, criticidade temporal e reducao de risco ou oportunidade. O tamanho do trabalho deve ser estimado de forma relativa pelo time.

**Como usar:** defina a escala, avalie os fatores em conjunto e documente por que um item tem maior custo de atraso. Nao use WSJF para esconder uma obrigacao legal, incidente critico ou dependencia que exige tratamento direto.

#### Matriz Valor x Esforco

Indicado para uma conversa visual e rapida quando nao ha dados suficientes para uma formula.

1. Liste as oportunidades ou itens.
2. Estime valor e esforco em uma escala simples, como baixo, medio e alto.
3. Posicione os itens na matriz.
4. Investigue os itens de alto valor e baixo esforco, sem ignorar riscos e dependencias.

Use a matriz como triagem inicial. Registre os motivos quando uma opcao fora do quadrante de ganhos rapidos for escolhida.

#### Kano

Indicado para entender como diferentes tipos de funcionalidade influenciam a satisfacao:

- **Basicos:** esperados; sua ausencia gera insatisfacao.
- **Desempenho:** quanto melhor atendidos, maior tende a ser a satisfacao.
- **Encantadores:** nao esperados, mas podem gerar grande satisfacao quando presentes.

**Como usar:** combine entrevistas ou pesquisas com observacao de comportamento. Nao trate um item como encantador apenas porque parece inovador; valide se existe valor para o usuario e se a capacidade basica do produto esta atendida.

### Discovery e definicao do problema

#### Entrevista com usuario

Indicado para compreender contexto, comportamento, dificuldades e resultados desejados.

**Como usar:** defina o que precisa aprender, selecione perfis relevantes, faca perguntas sobre experiencias reais e registre evidencias separadas de interpretacoes. Evite perguntar apenas se a pessoa gostaria de uma solucao especifica.

**Saida esperada:** necessidades, comportamentos, citacoes relevantes, padroes, contradicoes e perguntas para investigar.

#### 5 Porques

Indicado para aprofundar uma falha ou sintoma e buscar causas possiveis.

**Como usar:** descreva o fato observado, pergunte por que ele ocorreu e repita ate chegar a uma causa que possa ser investigada. Valide cada resposta com dados; nao trate a quinta resposta como causa verdadeira por regra.

#### JTBD (Jobs to Be Done)

Indicado para descrever o progresso que o usuario tenta realizar em determinado contexto.

Modelo: `Quando [situacao], quero [motivacao], para [resultado esperado].`

Use o JTBD para evitar que o time descreva apenas uma tela ou funcionalidade. Complemente com contexto, frequencia, alternativas atuais e barreiras.

#### Opportunity Solution Tree

Indicado para conectar um resultado desejado a oportunidades identificadas e alternativas de solucao.

Estruture como: **resultado** -> **oportunidades ou necessidades** -> **solucoes** -> **experimentos ou testes**.

**Como usar:** comece por um resultado mensuravel, agrupe evidencias em oportunidades, gere mais de uma solucao e escolha experimentos que reduzam as maiores incertezas. Evite preencher a arvore com funcionalidades antes de entender as oportunidades.

### Ideacao e UX

#### Brainstorming

Indicado para gerar alternativas quando o problema esta suficientemente compreendido.

**Como usar:** apresente o problema e as restricoes, gere ideias individualmente antes da discussao, adie julgamentos, combine ideias e finalize com criterios claros de selecao. Separe a fase de gerar da fase de avaliar.

#### Crazy 8s

Indicado para explorar rapidamente varias alternativas de fluxo ou interface.

**Como usar:** dobre uma folha em oito partes, defina um tempo curto e produza oito variacoes da mesma solucao ou fluxo. Depois, agrupe padroes e selecione ideias para prototipo. O objetivo e variedade, nao acabamento visual.

#### Jornada do Usuario

Indicado para visualizar etapas, objetivos, dores, pontos de contato e oportunidades ao longo de uma experiencia.

Registre: persona ou perfil, etapas, objetivo em cada etapa, comportamento, emocao ou dificuldade, canais, evidencias e oportunidades.

Use a jornada para encontrar pontos de atrito e dependencias entre areas. Nao a trate como verdade geral se foi construida com uma amostra limitada.

#### Service Blueprint

Indicado para servicos que dependem de pessoas, sistemas e operacoes alem da interface.

Mapeie acoes do usuario, pontos de contato, interacoes visiveis, bastidores, sistemas de suporte e evidencias geradas. E especialmente util para notificacoes, integracoes, analise, aprovacao, auditoria e atendimento.

#### User Story Mapping

Indicado para organizar a experiencia de ponta a ponta e definir cortes de entrega.

**Como usar:** coloque as atividades principais na ordem da jornada, decomponha tarefas e historias abaixo delas, depois marque uma primeira versao de entrega que permita aprender ou gerar valor. Nao use o mapa apenas como uma lista de funcionalidades.

### Especificacao e validacao

#### User Story e criterios de aceite

Use a User Story para expressar usuario, necessidade e beneficio:

`Como [perfil], quero [necessidade], para [beneficio].`

Complemente com regras e cenarios. Para comportamentos condicionais, use Gherkin:

```gherkin
Cenario: [resultado esperado]
	Dado que [contexto]
	Quando [acao]
	Entao [resultado observavel]
```

Inclua cenarios de sucesso, erro, vazio, permissao, duplicidade, atraso, cancelamento e integracao quando forem aplicaveis.

#### Prototipo e teste de usabilidade

Indicado para validar entendimento, fluxo e linguagem antes de construir.

**Como usar:** defina a hipotese, crie o menor prototipo capaz de responder a pergunta, escolha participantes representativos, observe tarefas reais e registre erros de compreensao. Nao use elogios gerais como evidencia de usabilidade.

#### HEART e metricas de experiencia

Indicado para acompanhar qualidade da experiencia apos uma mudanca. HEART organiza metricas em **Happiness**, **Engagement**, **Adoption**, **Retention** e **Task Success**.

**Como usar:** escolha somente dimensoes relacionadas ao objetivo, defina o sinal desejado, a metrica e a fonte de dados. Combine percepcao do usuario com comportamento observado e resultado de negocio; nao use uma metrica isolada como prova de sucesso.

### Modelo de registro do framework

Use este bloco no Planning, card ou documento de decisao:

```markdown
## Framework utilizado
- Pergunta que precisava ser respondida:
- Framework ou tecnica:
- Data e participantes:
- Dados e fontes utilizados:
- Premissas e limitacoes:
- Resultado ou recomendacao:
- Decisao tomada:
- Quando revisar:
```

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

- **Escopo:** usar este exemplo somente se a integracao estiver confirmada para a etapa atual; caso contrario, classificar como incremento posterior ou investigacao.
- **Problema:** uma informacao aprovada nao chega ao canal esperado ou chega sem dados necessarios.
- **Evidencias:** identificador da execucao, ambiente, horario, status exibido, log correlato e destino esperado. Nao incluir credenciais ou dados sensiveis.
- **Criterios de aceite:** confirmar sucesso, falha, retentativa, mensagem para o usuario, detalhe no log e preservacao da trilha de auditoria.

### Status generico na interface

- **Problema:** o usuario ve uma falha sem conseguir entender o proximo passo.
- **Discovery:** separar o que precisa ser compreendido pelo usuario do diagnostico que deve permanecer nos logs.
- **Resultado:** mensagem generica que orienta o proximo passo, identificador para suporte e log detalhado para diagnostico, sem expor causa tecnica ou informacao sensivel na interface.

Os exemplos sao ilustrativos. As regras vigentes devem ser confirmadas nas decisoes do MVP, na base de conhecimento e com as areas responsaveis.

## Modelo de card

```markdown
# [TIPO] Titulo orientado ao resultado

## Contexto e origem
- Status:
- Etapa: MVP | Incremento posterior | Pendente de validacao
- Status da informacao: Confirmada | Hipotese | Pendente de validacao
- Responsavel:
- Prioridade e justificativa:
- Severidade, quando for bug:
- Solicitante:
- Cliente, area ou usuario afetado:
- Modulo ou fluxo:
- Fonte, evidencia ou card relacionado:
- Data:

## Problema ou oportunidade
Descreva o que acontece, quem e afetado e qual e o impacto.

## Comportamento atual
- Dado de entrada:
- Passos para reproduzir ou executar:
- Comportamento observado:
- Comportamento esperado:

## Resultado esperado
Descreva o comportamento ou resultado que deve ser possivel observar.

## Eixos do negocio
- Interpretacao regulatoria necessaria:
- Acao operacional esperada:
- Evidencia ou auditoria necessaria:

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
- Seguranca e privacidade:

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

## Referencias externas recomendadas

Use estas fontes para aprofundar praticas de produto. Elas complementam este guia e nao substituem as decisoes, regras e fontes oficiais do EvertecReg.

| Fonte | Foco | Como usar |
|---|---|---|
| [Scrum Guide 2020](https://scrumguides.org/scrum-guide.html) | Fundamentos de Scrum, Product Owner, Product Backlog, Sprint Goal e Definition of Done | Consultar quando houver duvida sobre responsabilidades e eventos do Scrum |
| [Scrum.org: Product Owner](https://www.scrum.org/resources/product-owners) | Valor do produto, visao, backlog e trabalho com stakeholders | Apoiar o desenvolvimento da pratica de PO |
| [Atlassian: Product Management](https://www.atlassian.com/agile/product-management) | Discovery, estrategia, roadmap, priorizacao, metricas e colaboracao | Usar como referencia ampla para PM e times ageis |
| [Product Talk](https://www.producttalk.org/) | Continuous Discovery, entrevistas, teste de hipoteses e Opportunity Solution Tree | Apoiar investigacoes e validacoes antes da implementacao |
| [SVPG: Product Management - Start Here](https://www.svpg.com/product-management-start-here/) | Papel do PM, discovery e times orientados a resultados | Aprofundar estrategia e modelo de trabalho de produto |
| [Mind the Product](https://www.mindtheproduct.com/) | Artigos, podcasts, eventos e experiencias de profissionais de produto | Buscar casos, praticas e perspectivas diferentes |
| [ProductPlan Learning Center](https://www.productplan.com/learn/) | Entrevistas, priorizacao, roadmap, metricas e gestao de stakeholders | Consultar guias praticos e templates |
| [PM3](https://pm3.com.br/blog/) | Conteudo em portugues sobre PM, PO, discovery, analytics, growth e lideranca | Usar para referencias e exemplos no contexto brasileiro |

Ao consultar uma referencia externa, registre no card ou no documento de decisao apenas o aprendizado aplicavel ao contexto do produto. Framework, template ou pratica nao deve ser adotado automaticamente: avalie se resolve uma necessidade real do time e se e compativel com os acordos vigentes.
