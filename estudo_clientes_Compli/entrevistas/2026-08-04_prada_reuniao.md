# Registro de Entrevista — Prada

## Identificação

- **Data:** 04 de agosto de 2026
- **Cliente:** Prada (Gestora de Ativos)
- **Participantes:** 
  - Henrique (Prada)
  - Tatiana Dantas (Prada)
  - Rafael Faro (Compliasset — Engenharia)
  - Laura Silva (Compliasset — Comunicação)
- **Canal:** Videoconferência

---

## Objetivo da Conversa

Apresentar a iniciativa de IA do Compliasset (assistente integrado com modelo interno de IA) e colher feedback sobre funcionalidades propostas, casos de uso prioritários, e validar preocupações de segurança e isolamento de dados entre clientes.

---

## Contexto Relatado pelo Cliente

**Henrique (Prada)** relata:
- Já utilizam IA em sistema próprio de processamento com integração eficiente
- Experimento prévio: IA ajudou a identificar erro de parâmetro que ChatGPT genérico não havia detectado (imposto de renda em eventos de decisão/incorporação)
- Usam ChatGPT e Gemini para consultas mais genéricas de compliance
- **Insight crítico:** IAs contextualizadas (internas, com conhecimento específico da empresa) são muito mais úteis que IAs genéricas

**Sobre o Compliasset:**
- Módulos usados: agenda regulatória, background checks, monitoramento
- Background check atual é "simplista" — apenas retorna PDF bruto
- Recebem e-mail semanal genérico de tarefas a vencer (baixa priorização)

**Sobre a empresa:**
- Gestora de ativos com obrigações regulatórias críticas (ex.: CVM, que gera multas)
- Equipe de compliance com pressão de prazos e distinção entre obrigatório vs. recomendado

---

## Dores Principais

### 1. Alertas Genéricos Não Diferenciam Criticidade
- **Problema:** E-mail semanal lista tudo na mesma importância
- **Impacto:** Risco de perder alertas críticos entre informação genérica
- **Exemplo citado:** Obrigação CVM (multa) precisa alerta com semanas de antecedência; recomendação pode ter alerta menor

### 2. Background Check Muito Simples
- **Problema:** Hoje coloca CPF → recebe PDF, sem análise nem sugestões
- **Impacto:** Analista precisa fazer análise manual de cada resultado
- **Necessário:** Eliminação de homônimos, classificação por risco, relatório com score final

### 3. Tarefas Manuais Repetitivas
- Arquivo de atividades antigas exige múltiplos cliques
- Criação de atividades, eventos, treinamentos — todos via UI

### 4. Segurança e Isolamento de Dados (Crítico)
- **Preocupação:** Dados de Prada poderiam vazar para outro cliente ou vice-versa?
- **Validação necessária:** Como a Compliasset garante separação?
- **Impacto:** Tema bloqueador caso não seja resolvido

---

## Necessidades e Expectativas

### Prioridade 1 (Imediato)
- [ ] **Chat assistente integrado** que execute ações via prompt
  - Exemplo: "arquiva todas as atividades X, Y, Z"
  - Executar sem navegar pela UI
  - Aprender conteúdo da empresa conforme interage

- [ ] **Modelo de IA seguro (interno, não ChatGPT)**
  - Mantido em cloud privada
  - Separação lógica entre clientes garantida
  - Documentação jurídica validando isolamento

### Prioridade 2 (Próximas semanas)
- [ ] **Parametrização de antecedência de alertas**
  - Cada obrigação: tempo de aviso customizável
  - Exemplo: obrigação vence dia 31 → alerta a partir de dia 27
  - Diferenciação por tipo (crítica vs. recomendação)

- [ ] **Background check com análise IA**
  - Eliminação automática de homônimos
  - Classificação por risco (TEP fora do governo há +5 anos = médio risco)
  - Score final (alto/médio/baixo)
  - Sugestão de ações baseada em resultado

- [ ] **Visualização inteligente de prazos**
  - Estruturação do e-mail semanal por criticidade
  - Foco em itens urgentes/críticos

### Prioridade 3 (Roadmap Futuro)
- [ ] Monitoramento proativo (IA avisa sem depender de ação do usuário)
- [ ] Integração com IAs externas (se já usam ChatGPT/Claude)

---

## Trechos Relevantes

> "A gente está desenvolvendo um novo recurso de IA para deixar o sistema mais ágil e facilitar a rotina de vocês. A ideia é um assistente dentro da própria plataforma para ajudar os usuários a encontrar informações e executar atividades de forma mais rápida."
— Laura Silva (Compliasset)

> "Dentro do sistema deles, que sim, ajudou para a parte de compliance, que era uma questão de limites... a IA respondeu corretamente. Então foi super útil mesmo."
— Henrique, sobre experiência com IA contextualizada

> "Eu gostaria até de de meio que quase que fazer uma troca com a né passando digamos as características do negócio que a gente faz aqui para poder já aplicar eventualmente algumas mudanças."
— Henrique, propondo maior participação na evolução da IA

> "É um assistente que está plugado a todo o conteúdo que hoje existe dentro do Compliasset, da sua empresa, e ele permite que você faça praticamente todas as ações que hoje a gente tem na interface através de um prompt, como a gente usa um ChatGPT da vida."
— Rafael, explicando o modelo

> "Para a gente é bem importante isso [segurança de dados]..."
— Tatiana, sobre preocupação com isolamento entre clientes

---

## Oportunidades Identificadas

### 1. Early Adopter para MVP
- Prada demonstra **alta confiança** em IA
- **Entendimento claro** dos conceitos propostos
- **Disposição para testar** e fornecer feedback iterativo
- **Recomendação:** Incluir como um dos primeiros clientes no beta do chat

### 2. Validação de Parametrização de Alertas
- Henrique trouxe demanda **muito específica e bem-articulada**
- Outros clientes também mencionaram variantes (priorização)
- **Recomendação:** Usar Prada como validador de feature crítica

### 3. Integração de Background Check Avançado
- Prada já pesquisou soluções externas (fornecedores especializados)
- Conhece o que é possível (eliminação de homônimos, score de risco)
- **Recomendação:** Testar em Prada antes de rollout geral

### 4. Documentação de Segurança
- Prada levantou questão legítima e bem-feita
- Resposta técnica bem-recebida
- **Recomendação:** Usar Prada como validador de documentação de isolamento de dados

---

## Próximos Passos

### Curto Prazo (Próxima Semana)
- [ ] Rafael/Laura: Liberar acesso ao chat assistente para Prada (conforme prometido)
- [ ] Rafael/Laura: Enviar e-mail com credenciais e guia de uso
- [ ] Laura: Solicitar feedback inicial sobre facilidade de uso do chat

### Médio Prazo (2-3 Semanas)
- [ ] Equipe Jurídica: Preparar documentação de segurança/isolamento de dados para Prada
- [ ] Engenharia: Implementar parametrização de antecedência de alertas
- [ ] Engenharia: Liberar beta de background check com IA
- [ ] Rafael: Agendar reunião de feedback com Henrique + Tatiana

### Acompanhamento
- [ ] Registrar feedback de Prada no banco de feedback de clientes
- [ ] Monitorar uso do chat assistente (para avaliar adoção e gargalos)
- [ ] Validar satisfação com background check melhorado
- [ ] Incluir Prada em discussões futuras sobre evolução da IA (monitoramento proativo, etc.)

---

## Notas Internas

- **Engajamento:** Muito alto ✅
- **Compreensão técnica:** Boa (cliente já usa IA)
- **Disposição para feedback:** Alta
- **Risco de churn:** Muito baixo (satisfação com direção de roadmap)
- **Timeline esperada para feedback:** 1-2 semanas após liberação do chat
- **Tema crítico:** Segurança — bem resolvido na reunião, mas acompanhar documentação jurídica

---

**Próxima revisão:** Após 1ª semana de uso do chat  
**Registrado em:** 04/08/2026
