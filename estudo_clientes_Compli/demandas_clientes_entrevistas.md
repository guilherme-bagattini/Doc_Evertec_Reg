# Demandas de clientes extraídas das entrevistas

Documento de trabalho para análise e priorização. Cada item foi convertido em uma demanda técnica curta a partir de uma solicitação, desejo ou ideia mencionada nas entrevistas. A classificação na matriz é uma avaliação inicial para orientar a leitura e não representa decisão de roadmap.

## Como ler os cards

- **Empresa:** origem da fala do cliente.
- **Classificação na matriz:** avaliação inicial de valor e esforço para orientar a decisão.
- **Em termos simples:** tradução da demanda para facilitar a leitura pelo time.
- **O que fazer:** escopo inicial da demanda.
- **Objetivo:** resultado esperado para o cliente.
- **Problema:** dor ou contexto relatado.
- **Critério de aceite:** condição mínima para considerar a entrega funcional.

---

## Solicitações explícitas

### DEM-001 — Movimentação em lote de documentos

- **Empresa:** Algarve Investimentos
- **Classificação na matriz:** Alto Valor + Baixo Esforço
- **Em termos simples:** Selecionar vários arquivos e mover todos de uma vez, como no explorador de arquivos do computador.
- **O que fazer:** Permitir selecionar múltiplos documentos e movê-los para outra pasta em uma única operação.
- **Objetivo:** Reduzir o tempo gasto na organização do acervo.
- **Problema:** Arquivos precisam ser movidos individualmente; o cliente considera a movimentação em lote uma funcionalidade básica.
- **Critério de aceite:** Usuário consegue selecionar vários documentos, escolher a pasta de destino, confirmar a operação e visualizar o resultado sem perda de arquivos.
- **Origem:** [2026-07-03_algarve_investimentos_reuniao.md](entrevistas/2026-07-03_algarve_investimentos_reuniao.md)

### DEM-002 — Registro retroativo do histórico de compliance

- **Empresa:** AWR Capital
- **Classificação na matriz:** Alto Valor + Baixo Esforço
- **Em termos simples:** Registrar agora os controles de compliance que já aconteceram, mesmo que tenham ocorrido antes do uso da plataforma.
- **O que fazer:** Criar uma forma de registrar avaliações, comitês, alocações e demais eventos de compliance ocorridos no passado.
- **Objetivo:** Completar o histórico de compliance sem gerar tarefas futuras indevidas.
- **Problema:** Atividades foram realizadas, mas não documentadas na plataforma ao longo do ano.
- **Critério de aceite:** Usuário consegue informar data passada, tipo de evento e evidências; o registro aparece no histórico e não cria notificações retroativas na agenda.
- **Origem:** [2026-07-07_awr_capital_reuniao.md](entrevistas/2026-07-07_awr_capital_reuniao.md)

### DEM-003 — Data de corte para limpeza da agenda

- **Empresa:** AWR Capital
- **Classificação na matriz:** Alto Valor + Baixo Esforço
- **Em termos simples:** Escolher a partir de qual data a agenda deve começar a cobrar as obrigações futuras.
- **O que fazer:** Permitir definir uma data de corte para separar o passivo histórico da rotina futura de notificações.
- **Objetivo:** Iniciar o acompanhamento regulatório futuro com uma agenda limpa.
- **Problema:** O histórico acumulado mistura-se às obrigações futuras e contamina o fluxo operacional.
- **Critério de aceite:** Usuário informa a data de corte; itens anteriores são tratados como histórico/arquivados e itens posteriores permanecem na rotina futura, sem exclusão de dados.
- **Origem:** [2026-07-07_awr_capital_reuniao.md](entrevistas/2026-07-07_awr_capital_reuniao.md)

### DEM-004 — Integração com a API da Neo

- **Empresa:** Capsicum Assets
- **Classificação na matriz:** Alto Valor + Alto Esforço
- **Em termos simples:** Fazer a Compliasset consultar a Neo automaticamente, sem que o usuário precise trocar de sistema e importar arquivos.
- **O que fazer:** Integrar a Compliasset à API da Neo para consultar dados de risco de terceiros.
- **Objetivo:** Automatizar a coleta de informações hoje consultadas manualmente.
- **Problema:** O processo atual exige consultar a Neo, analisar o resultado e fazer upload na Compliasset; o esforço aumenta com o volume.
- **Critério de aceite:** Usuário autorizado inicia ou agenda uma consulta; a integração autentica na Neo, registra a solicitação e apresenta o retorno associado ao terceiro correto.
- **Origem:** [2026-07-08_capsicum_assets_reuniao.md](entrevistas/2026-07-08_capsicum_assets_reuniao.md)

### DEM-005 — Recebimento automático da classificação de risco

- **Empresa:** Capsicum Assets
- **Classificação na matriz:** Alto Valor + Alto Esforço
- **Em termos simples:** Receber o resultado da Neo e já mostrar na Compliasset o nível de risco calculado pela matriz do cliente.
- **O que fazer:** Receber pela API o resultado da análise da Neo e aplicar a matriz de risco configurada pelo cliente.
- **Objetivo:** Evitar classificação e upload manuais após cada consulta.
- **Problema:** A plataforma hoje não processa automaticamente o resultado de análises externas.
- **Critério de aceite:** Resultado recebido é validado, associado ao cadastro correto, classificado conforme a matriz e disponibilizado com histórico do processamento e erro identificável quando houver falha.
- **Origem:** [2026-07-08_capsicum_assets_reuniao.md](entrevistas/2026-07-08_capsicum_assets_reuniao.md)

### DEM-006 — Solução integrada de PLD

- **Empresa:** Capsicum Assets
- **Classificação na matriz:** Alto Valor + Alto Esforço
- **Em termos simples:** Criar dentro da plataforma um fluxo completo para executar e acompanhar as rotinas de PLD.
- **O que fazer:** Disponibilizar um fluxo ou módulo de Prevenção à Lavagem de Dinheiro (PLD) dentro da plataforma.
- **Objetivo:** Atender uma necessidade crítica do pipeline de compliance do cliente.
- **Problema:** PLD é uma necessidade atual não atendida pela solução existente.
- **Critério de aceite:** Usuário consegue executar o fluxo de PLD definido para o produto, registrar evidências, acompanhar pendências e consultar o histórico das análises.
- **Observação:** Necessidade explicitamente apontada como crítica pelo cliente.
- **Origem:** [2026-07-08_capsicum_assets_reuniao.md](entrevistas/2026-07-08_capsicum_assets_reuniao.md)

### DEM-007 — Aceite de políticas dentro da plataforma

- **Empresa:** Capsicum Assets
- **Classificação na matriz:** Alto Valor + Baixo Esforço
- **Em termos simples:** Enviar uma política para os usuários e saber quem leu e aceitou, sem controlar isso por e-mail ou planilha.
- **O que fazer:** Permitir publicar uma política, encaminhá-la aos usuários e registrar o aceite diretamente na Compliasset.
- **Objetivo:** Substituir o processo manual realizado fora da plataforma.
- **Problema:** O processo atual não é utilizado adequadamente porque o aceite acontece manualmente e fora do fluxo principal.
- **Critério de aceite:** Administrador publica a política, usuários recebem a solicitação, o aceite fica registrado com usuário e data e o administrador consulta pendências.
- **Origem:** [2026-07-08_capsicum_assets_reuniao.md](entrevistas/2026-07-08_capsicum_assets_reuniao.md)

### DEM-008 — Formulários de declarações regulatórias

- **Empresa:** Capsicum Assets
- **Classificação na matriz:** Alto Valor + Baixo Esforço
- **Em termos simples:** Usar a Compliasset para enviar, responder e acompanhar declarações obrigatórias dos colaboradores.
- **O que fazer:** Disponibilizar ou ativar formulários para declaração de embarque, conflito de interesse e investimentos pessoais.
- **Objetivo:** Centralizar declarações recorrentes no ambiente de compliance.
- **Problema:** O cliente desconhecia essas possibilidades e não tinha clareza sobre como realizar esses processos na plataforma.
- **Critério de aceite:** Usuário autorizado consegue localizar cada formulário, enviá-lo ao público definido, acompanhar respostas e consultar os registros enviados.
- **Origem:** [2026-07-08_capsicum_assets_reuniao.md](entrevistas/2026-07-08_capsicum_assets_reuniao.md)

### DEM-009 — Registro de desenquadramentos de transações

- **Empresa:** Daemon
- **Classificação na matriz:** Alto Valor + Alto Esforço
- **Em termos simples:** Transformar um desenquadramento em um caso rastreável, com responsável, evidências, prazo e conclusão.
- **O que fazer:** Criar um fluxo para registrar, analisar, tratar e concluir desenquadramentos de transações.
- **Objetivo:** Formalizar na plataforma um processo hoje controlado por e-mail e documento externo.
- **Problema:** O processo existe, mas não está centralizado nem rastreável no sistema.
- **Critério de aceite:** Usuário registra o caso, anexa evidências, atribui responsáveis, acompanha status e consulta o histórico até a conclusão.
- **Origem:** [2026-07-10_daemon_reuniao.md](entrevistas/2026-07-10_daemon_reuniao.md)

### DEM-010 — Centralização de denúncias

- **Empresa:** Daemon
- **Classificação na matriz:** Alto Valor + Alto Esforço
- **Em termos simples:** Registrar uma denúncia com acesso controlado e acompanhar seu tratamento até o encerramento.
- **O que fazer:** Criar um canal ou módulo para registrar e acompanhar denúncias de compliance dentro da plataforma.
- **Objetivo:** Centralizar o tratamento e aumentar a rastreabilidade dos casos.
- **Problema:** O procedimento relacionado ao programa de compliance não está formalizado na Compliasset.
- **Critério de aceite:** Usuário autorizado registra uma denúncia, controla acesso, acompanha status, inclui evidências e consulta o histórico de tratamento.
- **Origem:** [2026-07-10_daemon_reuniao.md](entrevistas/2026-07-10_daemon_reuniao.md)

### DEM-011 — Assistente de IA para execução de ações

- **Empresa:** Prada
- **Classificação na matriz:** Alto Valor + Alto Esforço
- **Em termos simples:** Digitar uma solicitação no chat e, após confirmar, deixar a IA executar a operação na plataforma.
- **O que fazer:** Criar um chat contextual capaz de interpretar comandos e executar ações autorizadas na plataforma.
- **Objetivo:** Reduzir navegação e trabalho repetitivo em operações como arquivar atividades ou criar registros.
- **Problema:** O cliente executa tarefas manuais repetitivas e considera uma IA contextualizada mais útil que uma IA genérica.
- **Critério de aceite:** Usuário autorizado informa um comando, o sistema apresenta o plano de ação e pede confirmação antes de executar; ao final, informa sucesso, falhas e itens afetados.
- **Observação:** Demanda apontada como prioridade alta.
- **Origem:** [2026-08-04_prada_reuniao.md](entrevistas/2026-08-04_prada_reuniao.md)

### DEM-012 — Isolamento de dados para solução de IA

- **Empresa:** Prada
- **Classificação na matriz:** Alto Valor + Alto Esforço
- **Em termos simples:** Garantir que a IA só consulte e use os dados do cliente que está fazendo a solicitação.
- **O que fazer:** Garantir isolamento lógico de dados, permissões e contexto entre clientes no uso de recursos de IA.
- **Objetivo:** Permitir adoção da IA sem risco de exposição cruzada de informações.
- **Problema:** O cliente questionou se dados de uma empresa poderiam aparecer para outro cliente.
- **Critério de aceite:** Testes comprovam que consultas de um cliente não acessam dados de outro; permissões são aplicadas no contexto da IA e a documentação de segurança descreve o isolamento.
- **Observação:** Pré-requisito bloqueador para recursos de IA.
- **Origem:** [2026-08-04_prada_reuniao.md](entrevistas/2026-08-04_prada_reuniao.md)

### DEM-013 — Antecedência configurável de alertas

- **Empresa:** Prada
- **Classificação na matriz:** Alto Valor + Baixo Esforço
- **Em termos simples:** Definir com quantos dias de antecedência cada tipo de obrigação deve gerar um alerta.
- **O que fazer:** Permitir configurar a antecedência dos alertas conforme a criticidade de cada obrigação.
- **Objetivo:** Dar mais tempo de reação para obrigações críticas e reduzir ruído em recomendações.
- **Problema:** O e-mail semanal trata itens de importâncias diferentes de maneira uniforme.
- **Critério de aceite:** Usuário configura antecedência por nível de criticidade ou obrigação; alertas são enviados no prazo configurado e respeitam preferências de canal e destinatário.
- **Origem:** [2026-08-04_prada_reuniao.md](entrevistas/2026-08-04_prada_reuniao.md)

### DEM-014 — Background Check com análise de IA

- **Empresa:** Prada
- **Classificação na matriz:** Alto Valor + Alto Esforço
- **Em termos simples:** Entregar uma análise interpretada do background check, em vez de apenas um PDF para leitura manual.
- **O que fazer:** Analisar automaticamente resultados de background check, eliminando homônimos e classificando risco.
- **Objetivo:** Reduzir a análise manual e apoiar a decisão do analista.
- **Problema:** O processo atual entrega um PDF bruto a partir do CPF; o analista precisa interpretar cada resultado manualmente.
- **Critério de aceite:** Sistema identifica possíveis homônimos, classifica o resultado como alto, médio ou baixo risco, apresenta justificativa e sugere ações para revisão humana antes da conclusão.
- **Origem:** [2026-08-04_prada_reuniao.md](entrevistas/2026-08-04_prada_reuniao.md)

### DEM-015 — E-mail de prazos organizado por criticidade

- **Empresa:** Prada
- **Classificação na matriz:** Alto Valor + Baixo Esforço
- **Em termos simples:** Reorganizar o e-mail para mostrar primeiro o que é crítico e depois o que pode esperar.
- **O que fazer:** Reestruturar o e-mail semanal de prazos para destacar itens críticos e urgentes antes dos demais.
- **Objetivo:** Fazer o usuário identificar rapidamente as obrigações que exigem ação.
- **Problema:** A listagem atual é genérica e não diferencia adequadamente prioridades.
- **Critério de aceite:** E-mail agrupa ou ordena itens por criticidade, destaca obrigações críticas e mantém acesso direto ao registro correspondente na plataforma.
- **Origem:** [2026-08-04_prada_reuniao.md](entrevistas/2026-08-04_prada_reuniao.md)

---

## Sugestões e interesses dos clientes

### DEM-016 — Simplificação da usabilidade da Agenda

- **Empresa:** Algarve Investimentos
- **Classificação na matriz:** Alto Valor + Alto Esforço
- **Em termos simples:** Tornar a Agenda mais fácil de entender, com menos complexidade e caminhos mais claros para executar as tarefas.
- **O que fazer:** Revisar a experiência da Agenda, reduzindo complexidade e tornando os principais fluxos mais intuitivos.
- **Objetivo:** Aumentar a autonomia do usuário no acompanhamento das atividades.
- **Problema:** A Agenda é percebida como complexa e pouco intuitiva; o cliente recorre a ferramentas de IA para validar atividades.
- **Critério de aceite:** Usuário consegue localizar, entender e executar uma atividade recorrente sem depender de orientação externa; testes de usabilidade validam os principais fluxos.
- **Origem:** [2026-07-03_algarve_investimentos_reuniao.md](entrevistas/2026-07-03_algarve_investimentos_reuniao.md)

### DEM-017 — Limpeza e revisão da Agenda

- **Empresa:** Hike Capital
- **Classificação na matriz:** Alto Valor + Baixo Esforço
- **Em termos simples:** Revisar a lista de atividades, marcar o que se aplica ao cliente e retirar o que não faz sentido da rotina.
- **O que fazer:** Permitir exportar a Agenda para revisão e identificar atividades que não se aplicam ao contexto operacional do cliente.
- **Objetivo:** Manter na Agenda somente obrigações relevantes para a empresa.
- **Problema:** O cliente percebe excesso de atividades e dificuldade para distinguir o que realmente precisa executar.
- **Critério de aceite:** Usuário consegue exportar a lista com informações suficientes para revisão, marcar itens aplicáveis ou não aplicáveis e visualizar o resultado da revisão.
- **Origem:** [2026-07-07_hike_capital_reuniao.md](entrevistas/2026-07-07_hike_capital_reuniao.md)

### DEM-018 — Arquivamento ou ocultação de atividades e seções

- **Empresa:** Hike Capital
- **Classificação na matriz:** Alto Valor + Baixo Esforço
- **Em termos simples:** Esconder atividades desnecessárias da visão principal sem apagar seus registros ou histórico.
- **O que fazer:** Permitir arquivar ou ocultar atividades e seções da Agenda sem excluir seus registros.
- **Objetivo:** Reduzir ruído na visão operacional preservando rastreabilidade.
- **Problema:** O cliente quer simplificar a Agenda, mas não pode perder o histórico ou os dados originais.
- **Critério de aceite:** Usuário autorizado arquiva ou oculta um item, o item deixa de aparecer na visão ativa, permanece pesquisável no histórico e pode ser restaurado.
- **Origem:** [2026-07-07_hike_capital_reuniao.md](entrevistas/2026-07-07_hike_capital_reuniao.md)

### DEM-019 — Background Check como ferramenta analítica

- **Empresa:** SVN
- **Classificação na matriz:** Alto Valor + Alto Esforço
- **Em termos simples:** Fazer o Background Check indicar o nível de risco e sugerir qual diligência deve ser feita em seguida.
- **O que fazer:** Evoluir o Background Check para classificar automaticamente o risco e recomendar diligências adicionais.
- **Objetivo:** Transformar uma fonte de dados em apoio efetivo à decisão de compliance.
- **Problema:** O processo atual apresenta informação, mas não consolida análise nem orientação para o próximo passo.
- **Critério de aceite:** Sistema classifica o terceiro como alto, médio ou baixo risco conforme regras configuradas, explica os fatores considerados e sugere diligências para validação do analista.
- **Origem:** [2026-08-07_svn_reuniao.md](entrevistas/2026-08-07_svn_reuniao.md)

### DEM-020 — Monitoramento proativo com IA

- **Empresa:** Prada
- **Classificação na matriz:** Alto Valor + Alto Esforço
- **Em termos simples:** Fazer a IA acompanhar eventos relevantes e avisar o usuário antes que ele precise procurar a informação.
- **O que fazer:** Criar mecanismo de IA que monitore alterações relevantes e envie alertas sem depender de uma consulta manual.
- **Objetivo:** Antecipar riscos e obrigações relevantes para o usuário.
- **Problema:** O sistema depende de ação do usuário para consultar informações e gerar alertas.
- **Critério de aceite:** Usuário configura temas ou eventos monitorados; o sistema identifica uma ocorrência, envia alerta com contexto e registra a origem da recomendação.
- **Observação:** Interesse indicado como possibilidade de roadmap futuro.
- **Origem:** [2026-08-04_prada_reuniao.md](entrevistas/2026-08-04_prada_reuniao.md)

### DEM-021 — Integração com IAs externas

- **Empresa:** Prada
- **Classificação na matriz:** Alto Valor + Alto Esforço
- **Em termos simples:** Conectar a Compliasset às IAs que o cliente já usa, com controle sobre quais dados podem sair da plataforma.
- **O que fazer:** Avaliar integração segura entre a Compliasset e ferramentas externas de IA já utilizadas pelo cliente, como ChatGPT e Claude.
- **Objetivo:** Evitar retrabalho e manter o fluxo de análise conectado às ferramentas adotadas pela equipe.
- **Problema:** O cliente já utiliza IAs externas e deseja continuidade entre esses recursos e os dados ou processos da Compliasset.
- **Critério de aceite:** Usuário autorizado consegue enviar ou consultar informações por integração documentada, com controle de permissões, registro da operação e proteção contra envio indevido de dados.
- **Observação:** Interesse indicado como possibilidade de roadmap futuro.
- **Origem:** [2026-08-04_prada_reuniao.md](entrevistas/2026-08-04_prada_reuniao.md)

---

## Resumo para priorização posterior

| Grupo | Cards | Leitura inicial |
|---|---:|---|
| Solicitações explícitas | 15 | Pedidos diretos ou necessidades operacionais claramente verbalizadas |
| Sugestões e interesses | 6 | Oportunidades percebidas, mas que exigem validação adicional |
| **Total** | **21** | Base inicial para análise de produto e engenharia |

### Pontos que merecem validação antes de entrar no backlog

- Confirmar se os formulários de declarações da Capsicum já existem e precisam apenas de ativação/onboarding.
- Definir escopo regulatório e responsabilidade humana da solução de PLD.
- Validar regras de criticidade e de classificação de risco com cada cliente antes de automatizar decisões.
- Confirmar requisitos jurídicos, técnicos e contratuais para recursos de IA e integrações externas.
- Separar demandas de descoberta/configuração de demandas que exigem desenvolvimento.
