# Transcrição — Reunião Prada | 04/08/2026

**Data:** 04 de agosto de 2026  
**Horário:** 20:03 (8:03 PM)  
**Duração:** 23m 30s  
**Participantes:** Henrique (Prada), Tatiana Dantas (Prada), Rafael Faro (Compliasset), Laura Silva (Comunicação)

---

## Resumo Executivo

Reunião de apresentação da iniciativa de IA do Compliasset com cliente Prada. Discussão focada em:
1. Assistente de IA integrado à plataforma (chat com capacidade de executar ações)
2. Monitoramento proativo e alertas customizados
3. Melhorias em background check com análise inteligente
4. Preocupações críticas com segurança e isolamento de dados entre clientes

**Conclusão:** Cliente demonstrou alto interesse no assistente integrado, validou roadmap proposto e expressou preocupações legítimas sobre segurança — respondidas com esclarecimentos técnicos.

---

## Principais Tópicos Discutidos

### 1. Apresentação Inicial da Iniciativa

**Laura Silva / Rafael Faro** apresentam o projeto de IA para o Compliasset:
- Objetivo: tornar o sistema mais ágil e facilitar a rotina dos clientes
- Formato: assistente dentro da própria plataforma
- Diferencial: modelo de IA próprio, mantido internamente (não terceirizado)

**Contexto:** Equipe já passou sugestões sobre o sistema com Evelyn (na semana anterior). Rafael e Laura trazem uma apresentação mais detalhada para colher feedback antes de decisão final de roadmap.

---

### 2. Experiência Atual de Prada com IA

**Henrique (Prada)** relata:
- Sistema próprio com processamento que habilita IA para compliance
- Já fizeram consulta interna que ajudou em questão de limites
- Exemplo: IA identificou corretamente um parâmetro errado no sistema (imposto de renda em eventos de decisão/incorporação) — informação mais precisa que outras fontes

**Uso de IAs externas:**
- ChatGPT e Gemini para consultas mais genéricas
- ChatGPT respondeu confirmação sobre regras de imposto de renda (validou conhecimento prévio)
- Gemini utilizado para consultas de escopo mais amplo

**Limitação percebida:** IAs externas fornecem respostas genéricas; IA dentro de sistema fechado (próprio) é mais útil porque contextualizada.

---

### 3. Conceito do Assistente Integrado

**Rafael apresenta o conceito:**
- Chat integrado que permite executar praticamente todas as ações disponíveis na interface via prompt
- Exemplo concreto: "arquiva todas as atividades tais" — executa comando sem necessidade de clicks manuais
- Assistente "aprende" conteúdo da empresa conforme interage

**Versão Beta atual:**
- Já pode executar ações (criar atividades, arquivar, criar eventos, enviar treinamentos, etc.)
- Ainda em fase de teste; pode ter erros
- Equipe espera feedback dos clientes para evoluir

---

### 4. Roadmap: Fase 2 — Monitoramento Proativo

**Rafael comunica evoluções previstas:**
- Primeira fase: assistente reactivo (depende de ação do usuário)
- Segunda fase: assistente proativo — antecipa, avisa, monitora automaticamente
  - Exemplo: "Henrique, está acontecendo isso aqui" — sem depender de busca manual do usuário
  - Criação automática de alertas

**Henrique valida e expande o conceito:**
- Propõe parametrização de "tempo de antecedência para alertas"
- Exemplo: obrigação que vence dia 31 → receber alerta a partir de dia 27
- Diferencial importante: não é alerta genérico, é customizado por tipo e criticidade de obrigação

---

### 5. Demandas Específicas de Prada

**a) Alertas Customizados por Antecedência**
- Henrique cita exemplo de obrigação CVM que gera multa
- Deseja alerta com grande antecedência (não no dia antes do vencimento)
- Preferência: alertas segmentados por impacto/criticidade

**Validação de Rafael:**
- Reconhece que outros clientes também mencionaram demanda similar
- Confirma que IA pode ajudar a classificar conteúdo e criar essas etiquetas de prioridade
- Promete incluir no roadmap

**b) Visualização Inteligente de Prazos**
- Complemento ao e-mail semanal atual
- E-mail genérico lista tarefas da semana; Henrique quer visão mais estruturada
- IA deveria focar itens críticos e urgentes, não bombardear com informação genérica

**c) Ajustes Simples, Iterativos**
- Henrique propõe focar em 3 primeiros itens antes de expandir
- Reconhece importância de testar e aplicar feedback contínuamente
- Sem pressa para implementações complexas

---

### 6. Questão de Custo

**Henrique pergunta:** Vai ter custo adicional?

**Rafael responde:** 
- Ideia é não ter custo nenhum por enquanto
- É uma relação de troca — cliente ajuda testando, Compliasset aprende e evolui

**Laura confirma:**
- Vai ser parte do sistema em si, não ferramenta adicional
- Integração nativa ao Compliasset

---

### 7. Segurança e Isolamento de Dados (Tema Crítico)

**Tatiana (Prada) questiona:**
- Informações serão sigilosas?
- Tem risco de acesso a dados de outros clientes ou vice-versa?

**Rafael responde com detalhe técnico:**
- Inicialmente consideraram usar ChatGPT, mas descartaram por questões de segurança
- Optaram por modelo de IA interno (mais caro, mas necessário)
- Separação lógica garantida: cada cliente tem "caixinha" isolada
- Dados de um cliente NUNCA se misturam com outros
- Time jurídico também acompanhando para garantir compliance

**Acompanhamento:**
- Time está trabalhando em como demonstrar essa segurança para clientes
- Documentação será fornecida para evidenciar modelo de isolamento

**Prada manifesta satisfação:** "Para a gente é bem importante isso"

---

### 8. Background Check — Melhoria Proposta

**Contexto:** Henrique havia mencionado antes (reunião anterior) que gostaria de evolução maior no módulo de background check.

**Problema atual:** Hoje é "simplista" — coloca CPF, recebe relatório bruto sem análise.

**Sugestão de Prada:**
- Fornecedores especializados oferecem serviço mais completo
- Exemplos:
  - Eliminam homônimos (não confundem pessoas com mesmo nome)
  - Classificação automática baseada em parâmetros definidos
  - Análise inteligente: "essa pessoa é TEP, mas saiu do governo há +5 anos" = risco moderado
  - Relatório final com score consolidado (alto/médio/baixo)

**Validação de Rafael:**
- Já tem algo saindo "quase pronto" nesse sentido
- IA vai analisar background checks: não só retornar PDF, mas analisar conteúdo
- Estão expandindo fontes de dados (Avertek Compliance mencionado)
- Recurso de recorrência: "quero monitorar essa pessoa 1x/semana ou 1x/mês" — automático
- "Praticamente pronto para testes"

**Diferencial esperado:** De "tool que só gera PDF" para "ferramenta que analisa, classifica e sugere ações"

**Henrique valida:** "Que bom saber que tem algo evoluindo" — reconhece alinhamento entre demanda e roadmap.

---

### 9. Timeline de Disponibilização

**Tatiana pergunta:** Vocês têm previsão de colocar isso no ar para uso dos clientes?

**Rafael responde:**
- Chat assistente: **próxima semana no máximo** (05-11 de agosto)
- Clientes será um dos primeiros a testar

**Laura complementa:**
- Mandará e-mail com acesso quando estiver disponível
- Pedir feedback dos clientes sobre o que funcionou, o que pode melhorar
- Tudo que foi conversado está anotado e será considerado

---

## Pontos Finais

### Decisões Tomadas
1. ✅ Prada será um dos primeiros clientes a testar o assistente de chat (próxima semana)
2. ✅ Feedback será coletado através de reuniões contínuas
3. ✅ Priorizando 3 primeiros itens: alertas customizados, visualização de prazos, arquivo de atividades
4. ✅ Background check com IA será validado em testes posteriores
5. ✅ Documentação de segurança/isolamento será preparada pelo time jurídico

### Compromissos da Compliasset
- Liberar chat na próxima semana (máximo)
- Implementar parametrização de antecedência de alertas "nas próximas semanas"
- Manter contato contínuo para colher feedback
- Documentar garantias de segurança e isolamento de dados

### Nível de Engajamento
- **Alto:** Prada demonstrou compreensão clara do conceito, validou direção estratégica, levantou questões técnicas legítimas, pronto para testar
- **Segurança:** Tema crítico bem-gerenciado; cliente satisfeito com respostas

---

## Anexo: Conceitos-chave Mencionados

- **"Oráculo"** (de AZ Quest, não Prada, mas mencionado como referência): skill de Claude alimentada com políticas internas
- **Chat assistente:** versão 1, reativo; versão 2, proativo
- **Isolamento de dados:** modelo interno vs. externo; "caixinhas" isoladas por cliente
- **Background check evolution:** de PDF simples para análise inteligente com score
- **Parametrização de alertas:** diferencial importante de UX — customização por tipo/risco

---

**Documento preparado:** 04/08/2026  
**Referência:** Reunião Iniciativa IA · Prada
