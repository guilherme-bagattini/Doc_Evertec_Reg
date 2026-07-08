# Transcrição - Reunião Capsicum Assets

**Data:** 2026-07-08  
**Duração:** 21m 54s  
**Arquivo:** Capsicum e Compliasset-20260708_095904

**Participantes:**
- Laura Silva (Compliasset - líder comercial)
- Evelyn Ferraz (Compliasset - especialista em sistema)
- Guilherme Bagattini (Compliasset - analista de produto)
- Alice Frerichs (Capsicum Assets - decision maker)
- Ana Carolina Oliveira Reis (NPL Brasil/Capsicum - operacional de compliance)

---

## Resumo executivo

Reunião crítica revelou desalinhamento profundo entre escopo contratado e uso real. Capsicum usa apenas cadastro e upload de resultados de análises externas (Neo), realiza compliance fora do sistema, enfrenta agenda poluida desde dezembro de 2024. Alice deu feedback crítico: **falta de parametrização no onboarding deixou a plataforma um "monstrengo" difícil de manejar**. Risco iminente de churn/migração de plataforma. Proposta de ação rápida foi aceita: limpeza de agenda, integração Neo via API, PLD, treinamentos.

---

## Principais revelações

### 1. Modelo de uso real vs. esperado

**Esperado (contratação):**
- Ferramenta completa para acompanhamento regulatório
- Obrigações, compliance, pesquisa integrada

**Realizado:**
- Apenas cadastro de colaboradores
- Upload de resultados de análises externas (plataforma Neo)
- Ana (operacional) usa só para cadastro e entrada de dados

**Citação Alice:**
> "Na verdade, a minha primeira proposta era usar o Compli como uma ferramenta para nos ajudar em toda a parte regulatória, do acompanhamento das obrigações e também nessa parte compliance. A verdade é que hoje a gente usa basicamente só a parte compliance."

**Fluxo real de compliance:**
1. Análises feitas em plataforma parceira (Neo) 
2. Resultados/relatórios inseridos no Compliasset para registro
3. Compliasset usado apenas como repositório

### 2. Raiz do problema: excesso de informação + falta de parametrização no onboarding

**Problema central:** 
- Plataforma entrega conteúdo muito amplo e genérico
- Não personalizado para escopo real da Capsicum
- Falta total de parametrização no onboarding deixou agenda extremamente poluida desde dezembro de 2024

**Citações Alice:**
> "Tem tanta informação, tanta informação, tanta informação que fica difícil de usar"

> "Ela não é voltada às nossas necessidades. Então tem muita coisa ali que não tem nada a ver com os nossos fidics, não tem nada a ver com os nossos fundos."

### 3. Agenda poluida - volume paralisante

**Status:** Aberta desde dezembro de 2024, nunca foi limpa

**Citação Alice:**
> "Mas tem tanta coisa para [arquivar]... Tem uma hora que, poxa, você é difícil, sabe? Fica muito poluído."

**Reconhecimento Alice:**
> "Na verdade, para a gente começar a usar, tinha que reiniciar geral assim."

**Proposta Compliasset acordada:**
- Evelyn vai puxar relatório do que têm em agenda
- Capsicum indica o que quer arquivar
- Reinicializar agenda a partir de data preferida (ex: 1º de junho de 2026)

### 4. Descasamento de escopo/módulos

**Módulos contratados:**
- Gestor de FIDC
- Gestor de FII
- Gestor de Recursos

**Questão Alice:**
> "Qual que é a diferença dessa contratação? Porque hoje a gente tem FIDC, a gente tem FIDC e o IFM agros... Ou a gente não precisaria dele, a gente precisaria só do decidir aqui de Fiagra, considerando o nosso escopo de atuação hoje?"

**Explicação Evelyn:**
- Gestor de Recursos é a "base" (políticas, cibersegurança, privacidade)
- FIDC/FII são "módulos complementares"

**Ação:** Revistar se os 3 módulos fazem sentido para escopo atual

### 5. Análise de compliance não atendida por Compliasset

**Problema:**
- Compliasset não oferece análise de compliance adequada
- Capsicum usa Neo por ser mais completo e mais barato

**Citação Alice:**
> "A gente tentou puxar pela plataforma algumas vezes, mas sim, ela não atende o que a gente precisa, não vê os números, os processos, os processos completinhos. Acho que ainda falta muita informação"

**Citação Ana:**
> "Seria legal se a plataforma oferecesse também para a gente o relatório para ficar em um lugar só. A gente não precisar usar 2 plataformas para poder fazer o compliance."

**Por que Neo é melhor:**
- Análise mais completa
- Mais barato do que pesquisa reputacional Compliasset (R$15 CPF, R$25 CNPJ)

**Ferramenta de pesquisa reputacional Compliasset:**
- Terceirizada
- "Uma cesta fechada" - não conseguem adicionar outras fontes
- Custo fixo por consulta

### 6. Demanda crítica: Integração Neo via API

**Demanda Alice:**
> "A gente está pensando em fazer uma automatização lá com o time da Neo, a gente está discutindo fazer consultas por API e já vinha com o resultado de acordo com a nossa matriz de risco. Vocês conseguiram integrar também a plataforma de vocês com essa ponta da Neo? Para puxar relatório, já fazer a classificação de acordo com a indicação no relatório deles."

**Resposta Evelyn:**
> "A gente tem uma API, mas ela não faz esse tipo de integração. A API que a gente tem, ela é muito básica para criação de atividades, criação de eventos, cadastros. Então a gente não tem essa opção de integração."

**Ação:** Guilherme vai analisar viabilidade de ampliação da API

### 7. Automação de workflow compliance é prioridade

**Fluxo manual atual:**
1. Bater CPF/CNPJ na plataforma (Neo)
2. Tirar o relatório
3. Dar uma olhada
4. Bater com a matriz de risco
5. Pegar o resultado
6. Botar dentro do Compliasset
7. Fazer upload no sistema da Compliance
8. Marcar o risco

**Citação Alice:**
> "Ficar batucando o CPF, CNPJ na plataforma, tira o relatório, dá uma olhada, aí bate com a matriz e pega isso, bota dentro do sistema, faz o upload no sistema da Compliance, ele vai lá, marca o risco."

**Visão Alice para futuro:**
> "Conforme o volume cresce, a tendência é automatizar as funções e as atividades aqui. E aí ficar muito mais ligado no que for apresentar um red flag ou um risco diferente do baixo. Vai ficar muito mais analítico e menos operacional. A gente queria aliviar um pouco desse operacional."

> "Então, se a gente tivesse uma automatização disso, seria melhor."

### 8. Subutilização massiva de funcionalidades

**Treinamentos:**
- Alice: "Confesso que eu nem lembrava que tinha isso na plataforma"
- Evelyn ofereceu licenças para teste (cibersegurança, ASG, outros)

**Aceites e formulários:**
- Alice: "A gente faz manual, eles não aceitam, a gente sabe o documento, a gente nem usa para isso, a gente só cadastra os colaboradores e o aceite está em outro lugar."
- Evelyn menciona: embarque de colaborador, conflito de interesse, declaração de investimento pessoal

**Capacidade centralização não explorada:**
> "O objetivo mesmo do sistema é realmente isso, conseguir centralizar os processos que você tem dentro da plataforma. E se vocês não estão conseguindo fazer isso, estão precisando de outras ferramentas por fora, então a gente não está conseguindo atingir o nosso objetivo com vocês"

### 9. Urgência de PLD

**Citação Alice:**
> "Hoje que a gente precisa mesmo, que está no nosso pipeline de PLD, aí não sei se já podem mandar uma proposta."

**Ação:** Evelyn vai estruturar proposta de PLD

---

## Propostas e próximos passos acordados

### Ação 1: Limpeza e reinicialização de agenda

**Responsável:** Evelyn  
**Timeline:** Imediato

1. Puxar relatório do que Capsicum tem em agenda/obrigações (pode ser por planilha)
2. Capsicum analisa e indica o que arquivar
3. Capsicum indica data preferida para reinicializar (ex: 1º junho 2026)
4. Compliasset realiza limpeza e arquivamento

### Ação 2: Revisão de módulos contratados

**Responsável:** Evelyn + Guilherme  
**Escopo:** Validar se FIDC, FII, Recursos são necessários ou se precisam de outros

### Ação 3: Licenças de treinamento para teste

**Responsável:** Evelyn  
**Temas:** Cibersegurança, ASG, outros

### Ação 4: Aceites e formulários integrados

**Responsável:** Evelyn  
**O que migrar:**
- Aceites de políticas (atualmente manual)
- Formulários de declaração (embarque, conflito, investimentos)

### Ação 5: Análise integração Neo via API

**Responsável:** Guilherme (Produto)  
**Demanda:** Consultas por API + classificação automática de risco

### Ação 6: Proposta de PLD

**Responsável:** Evelyn + Guilherme  
**Contexto:** No pipeline de Alice

### Ação 7: E-mail consolidado

**Responsável:** Laura  
**Conteúdo:** Consolidação da reunião, propostas, timeline

---

## Feedback crítico sobre onboarding

**Alice (CRÍTICO):**
> "Se eu puder deixar esse feedback para vocês, acho que essa parametrização é essencial no onboarding. Se você deixa isso passar, a plataforma vira um \"monstrengo\" difícil de manejar, sabe?"

> "Se a gente pudesse contar um pouco mais das nossas, das nossas necessidades aqui e esse primeiro onboarding de vocês já viesse com essa visão do que realmente é necessário, acho que talvez a gente tivesse uma outra experiência com a plataforma."

**Evelyn (Resposta):**
> "Esse serviço de parametrização veio justamente por isso, para pegar mesmo na mão e vamos começar juntos, sabe? Vamos deixar ali a casa organizada, cadastro, documentos para vocês poderem iniciar ali."

**RECOMENDAÇÃO PARA PRODUTO:** Redesenhar onboarding para incluir parametrização como etapa **obrigatória** (não opcional) no início

---

## Context crítico: Ameaça de churn

**Citação Alice (implícita em ameaça):**
> "Na verdade, eu estou hoje bem pensando em descontinuar o serviço ou trocar por uma plataforma que já nos atenda junto com a parte de compliance também."

Este é um cliente em risco iminente de migração se ações não forem rápidas.

---

## Observações sobre qualidade

- Transcrição de reconhecimento de fala com algumas imprecisões ("Okay", "I" isolados, palavras mal capturadas)
- Pontos substantivos foram validados
- Estrutura consolidada para análise executiva
