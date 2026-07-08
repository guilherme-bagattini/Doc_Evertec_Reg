# Classificacao de clientes por utilizacao, risco e maturidade

## Objetivo

Criar uma classificacao simples para organizar clientes por nivel de uso da plataforma, risco de churn ou perda de valor e maturidade de compliance, sem perder de vista excecoes de contexto, como clientes em fase pre-operacional.

## Modelo recomendado

Sim, esse formato e util porque separa tres perguntas diferentes:

- quanto o cliente usa o sistema
- qual o risco comercial ou de churn
- em que estagio de maturidade de compliance o cliente esta

Usar apenas estrela para tudo tende a confundir pouco uso com baixo potencial. O caso da Nivi mostra isso com clareza: uso muito baixo, mas risco diferente de um cliente antigo frustrado.

## Utilizacao

### 5 estrelas

Muito alta. Cliente com uso forte e recorrente da plataforma, com sinais claros de incorporacao do sistema a rotina operacional.

### 4 estrelas

Alta. Cliente com uso consistente, ainda que nao total, com boa aderencia e sinais saudaveis de continuidade.

### 3 estrelas

Media. Cliente com uso intermediario, utilizando partes relevantes da plataforma, mas com espaco claro para expansao, reciclagem ou reorganizacao.

### 2 estrelas

Baixa. Cliente com baixo uso, mas com abertura concreta para retomada, ativacao ou reorganizacao. Ainda nao e um caso tipico de churn, mas exige acompanhamento.

### 1 estrela

Muito baixa. Cliente com uso muito baixo ou praticamente inexistente. Em muitos casos indica risco relevante de churn ou perda de valor percebido, mas precisa ser lido junto com risco e contexto.

## Risco

### Verde

Baixo risco. Cliente saudavel ou com justificativa clara para o nivel atual de uso.

### Amarelo

Medio risco. Cliente que precisa de acompanhamento para nao esfriar, atrasar ativacao ou perder aderencia.

### Vermelho

Alto risco. Cliente com sinais de frustracao, baixo valor percebido, risco de churn, comparacao desfavoravel com alternativas externas ou desconexao entre compra e uso.

## Maturidade compliance

### Nivel 1: Estruturacao

Empresa ainda montando base, processos, regulamentos, papeis e rotinas.

### Nivel 2: Basico

Ja possui estrutura minima, mas ainda opera de forma pouco sistematizada e com controles em consolidacao.

### Nivel 3: Intermediario

Tem rotinas definidas, controles recorrentes e comeca a buscar organizacao mais consistente.

### Nivel 4: Avancado

Opera com controles maduros, rotina estabelecida, governanca clara e uso mais disciplinado das ferramentas.

### Nivel 5: Estrategico

Compliance atua como funcao estrategica, integrada ao negocio, com alto nivel de organizacao, visibilidade e capacidade de evolucao.

## Excecoes

Nem todo cliente de 1 estrela deve ser tratado como churn.

Exemplo de excecao:

- cliente recente
- cliente em fase pre-operacional
- cliente ainda sem operacao iniciada
- cliente que contratou para credenciamento e ainda nao chegou ao momento de uso recorrente

Nesses casos, o ideal e marcar como `1 estrela - excecao de maturidade` ou `1 estrela - pre-operacional` e separar isso de risco.

## Regra de prioridade de atencao

Utilizacao mede uso. Risco mede urgencia. Maturidade mede contexto. Prioridade mede onde vale atuar primeiro.

### Prioridade alta

- cliente 1 ou 2 estrelas sem justificativa operacional forte
- cliente com baixa utilizacao e sinais de frustracao com o produto
- cliente com risco de churn, perda de aderencia ou comparacao desfavoravel com concorrentes e IA
- cliente com oportunidade concreta de reativacao no curto prazo

### Prioridade media

- cliente com baixo uso, mas com motivo justificavel e previsao concreta de ativacao
- cliente em fase de estruturacao, onboarding ou pre-operacao

### Prioridade baixa

- cliente com uso saudavel e sem sinais de risco imediato

## Classificacao inicial dos clientes mapeados

| Cliente | Utilizacao | Risco | Maturidade | Prioridade | Leitura resumida |
| --- | --- | --- | --- | --- | --- |
| Capsicum Assets | 1 estrela | Vermelho | Nivel 2 | Urgente | Desengajamento claro, ameaca de descontinuacao, ja em contato com concorrentes, demanda urgente de personalizacao, PLD e automacoes. |
| Algarve Investimentos | 1 estrela | Vermelho | Nivel 3 | Alta | Cliente antigo, baixo uso, percepcao de perda de aderencia do produto, comparacao desfavoravel com IA e insatisfacao com Documentos. |
| AWR Capital | 2 estrelas | Amarelo | Nivel 2 | Alta | Baixo uso, mas com interesse real em retomar, abertura para treinamento e chance concreta de ativacao. |
| Nivi Capital | 1 estrela - excecao pre-operacional | Amarelo | Nivel 1 | Media | Nao usa porque ainda nao iniciou a operacao. Ha intencao de uso quando houver captacao, crescimento da equipe e inicio dos fundos. |

## Qual cliente merece mais atencao agora

### 1. Capsicum Assets

E o caso mais critico e urgente.

Motivos:

- desengajamento claro com a plataforma
- ameaca explicita de descontinuacao
- ja em contato com concorrentes
- pressao para melhorias urgentes
- conhecimento incompleto do que o Compliasset oferece
- risco iminente de perder o contrato
- demandas especificas nao atendidas (PLD, automacoes, APIs)

### 2. Algarve Investimentos

E o segundo caso mais sensivel neste momento.

Motivos:

- cliente antigo
- baixo uso persistente
- valor percebido em queda
- comparacao direta com IA como alternativa superior
- friccao funcional no modulo de Documentos
- risco mais claro de churn ou downgrade de relevancia

### 2. AWR Capital

E o melhor caso de ativacao no curto prazo.

Motivos:

- nao ha rejeicao ao produto
- cliente recebeu bem propostas de treinamento e organizacao
- time pequeno, mas com disposicao para retomar uso
- oportunidade concreta de aumentar engajamento

### 3. Nivi Capital

Exige acompanhamento, mas nao com o mesmo senso de urgencia de churn.

Motivos:

- baixo uso esta explicado pelo momento do negocio
- cliente ainda nao precisou operar controles
- ha expectativa de comeco de operacao em dois ou tres meses
- vale preparar o terreno e acompanhar a transicao

## Recomendacao pratica para o futuro

Ao classificar novos clientes, registrar sempre seis campos:

- utilizacao
- risco
- maturidade compliance
- prioridade de atencao
- motivo principal do baixo ou alto uso
- proximo gatilho de acao

Exemplo:

- `1 estrela | vermelho | nivel 3 | prioridade alta | frustracao com produto | revisar agenda e modulos`
- `1 estrela - excecao pre-operacional | amarelo | nivel 1 | prioridade media | ainda sem operacao | acompanhar inicio da captacao`
- `2 estrelas | amarelo | nivel 2 | prioridade alta | interesse em retomada | agendar treinamento`