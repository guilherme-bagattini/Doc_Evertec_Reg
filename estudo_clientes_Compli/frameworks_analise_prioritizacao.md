# Frameworks para Análise e Priorização de Problemas - Dados Clientes Compliasset

## Objetivo
Após coletar dados de clientes, aplicar frameworks estruturados para:
1. **Elencar problemas recorrentes** com clareza
2. **Priorizar ações** com base em impacto/esforço
3. **Identificar quick wins** para entregar valor rapidamente
4. **Definir roadmap** de produto/comercial

---

## 🎯 FRAMEWORKS RECOMENDADOS (Aplicáveis aos Dados Coletados)

### 1. **Value vs Effort Matrix** (Prioritização Rápida)
**Uso:** Classificar ações/features em 4 quadrantes

**Quadrantes:**
- **Quick Wins** (Alto valor, Baixo esforço) → Implementar imediatamente
- **Strategic** (Alto valor, Alto esforço) → Planejar cuidadosamente
- **Fill-in** (Baixo valor, Baixo esforço) → Fazer quando houver tempo
- **Avoid** (Baixo valor, Alto esforço) → Não fazer

**Aplicação aos seus dados:**
```
QUICK WINS:
✓ Licenças treinamento Capsicum (2-3 dias)
✓ Puxar relatório agenda (1 dia)
✓ Templates por vertical (2 semanas)
✓ Agendar treinamento AWR (1 dia)

STRATEGIC:
✓ Integração Neo via API (4-6 semanas)
✓ Redesenho onboarding com parametrização obrigatória (3-4 semanas)
✓ PLD módulo/capacidade (6-8 semanas)

FILL-IN:
- Ajustes UI
- Correções bugs menores
- Documentação secundária

AVOID:
✗ Suporte múltiplos idiomas
✗ Features obsoletas
✗ Redesign gráfico completo
```

**Resultado esperado:** 8 quick wins identificados, 3 ações estratégicas estruturadas

---

### 2. **Eisenhower Matrix** (Urgência vs Importância)
**Uso:** Definir o que fazer AGORA vs. depois

**Quadrantes:**
- **Importante + Urgente** → Fazer agora (máxima prioridade)
- **Importante + Não-urgente** → Agendar/Planejar
- **Não-importante + Urgente** → Delegar
- **Não-importante + Não-urgente** → Eliminar

**Aplicação:**
```
FAZER AGORA (Próximas 2 semanas):
1. Limpeza agenda Capsicum
2. Licenças treinamento
3. Agendar treinos (AWR, Hike)
4. Análise viabilidade integração Neo API (início)
5. Proposta PLD (estrutura)

PLANEJAR (Próximas 4 semanas):
- Redesenho onboarding completo
- Desenvolvimento integração Neo
- Desenvolvimento PLD
- Melhorias análise compliance

DELEGAR:
- Ajustes menores UI
- Correções bugs
- Documentação

ELIMINAR:
- Features que não agregam
```

---

### 3. **MoSCoW Method** (Priorização de Features/Roadmap)
**Uso:** Classificar o que é essencial vs. nice-to-have

**Categorias:**
- **MUST** (Must Have) = Não pode ficar sem
- **SHOULD** (Should Have) = Deveria ter
- **COULD** (Could Have) = Seria legal ter
- **WON'T** (Won't Have now) = Não vai fazer agora

**Aplicação ao seu roadmap 2026 Q3:**
```
MUST:
✓ Redesenho onboarding (parametrização obrigatória)
  - Impacto: Previne problemas como Capsicum
  - Owner: Produto
  - Timeline: 3-4 semanas

✓ Integração Neo via API
  - Impacto: Salva Capsicum de churn
  - Owner: Desenvolvimento
  - Timeline: 4-6 semanas

SHOULD:
✓ Módulo/Capacidade PLD
  - Impacto: Atender demanda Capsicum
  - Owner: Produto + Comercial
  - Timeline: 6-8 semanas

✓ Melhorar análise compliance (mais fontes)
  - Impacto: Retirar uso de concorrentes
  - Owner: Produto
  - Timeline: 4-6 semanas

✓ Templates de uso por vertical
  - Impacto: Reduzir confusão escopo
  - Owner: Sucesso do Cliente
  - Timeline: 2 semanas

COULD:
- Ampliação API (eventos customizados)
- Dashboard visual de riscos
- Mobile app

WON'T (agora):
✗ Suporte múltiplos idiomas
✗ Integrações com 20+ sistemas
✗ Redesign gráfico completo
```

---

### 4. **Kano Model** (Satisfação do Cliente)
**Uso:** Entender o que gera satisfação vs. insatisfação

**Categorias:**
- **Satisfiers** (Features esperadas) = Causa insatisfação se faltar
- **Delighters** (Features surpresa) = Gera satisfação, não esperadas
- **Neutrals** = Não afeta satisfação

**Aplicação:**

```
SATISFIERS (Esperado, causa insatisfação se faltar):
- Onboarding claro com parametrização
- Agenda limpa e organizada
- Suporte responsivo
- Análise de compliance adequada
- Relatórios

⚠️ GAPS ENCONTRADOS:
Capsicum, AWR, Hike = insatisfação porque faltam satisfiers

DELIGHTERS (Surpresa positiva):
✓ Treinamento incluído
✓ Limpeza de agenda assistida
✓ Parametrização personalizada
✓ Integração com plataformas externas

NEUTRALS:
- Themes color
- Certificados de conclusão
- Gamification

AÇÃO: Converter satisfiers em delighters = aumentar satisfação
Exemplo: Transformar "onboarding básico" em "onboarding parametrizado + limpeza assistida"
```

---

### 5. **RICE Method** (Priorização com scoring)
**Uso:** Score numérico para priorizar features/ações

**Fórmula:** `(Reach × Impact × Confidence) / Effort`

**Como usar:**
```
Reach = Quantos usuários/clientes afeta (1-100)
Impact = Quanto muda a situação (1=mínimo, 3=médio, 10=máximo)
Confidence = Certeza da estimativa (10%-100%)
Effort = Horas/semanas necessárias
```

**Aplicação aos seus dados:**

```
INTEGRAÇÃO NEO API
- Reach: 1 cliente (Capsicum) = 10
- Impact: Evita churn, automatiza workflow = 10
- Confidence: 80% (viável mas precisa validação técnica) = 0.8
- Effort: 4-6 semanas = 40 dias
- SCORE: (10 × 10 × 0.8) / 40 = 2.0 ⭐⭐

REDESENHO ONBOARDING (Parametrização obrigatória)
- Reach: 5 clientes (todos) = 100
- Impact: Previne problemas estruturais = 10
- Confidence: 95% (clara necessidade) = 0.95
- Effort: 3-4 semanas = 24 dias
- SCORE: (100 × 10 × 0.95) / 24 = 39.6 ⭐⭐⭐⭐⭐ (TOP)

LIMPEZA AGENDA CAPSICUM
- Reach: 1 cliente = 10
- Impact: Demonstra valor, reduz frustração = 10
- Confidence: 100% (claro escopo) = 1.0
- Effort: 1 semana = 7 dias
- SCORE: (10 × 10 × 1.0) / 7 = 14.3 ⭐⭐⭐

LICENÇAS TREINAMENTO
- Reach: 3 clientes (Capsicum, AWR, Hike) = 30
- Impact: Mostra features, aumenta confiança = 10
- Confidence: 100% = 1.0
- Effort: 2-3 dias = 2 dias
- SCORE: (30 × 10 × 1.0) / 2 = 150 ⭐⭐⭐⭐⭐ (TOP)

RANKING FINAL:
1. Licenças treinamento (150) - FAZER PRIMEIRO
2. Redesenho onboarding (39.6) - ESTRATÉGICO
3. Limpeza agenda Capsicum (14.3) - RÁPIDO
4. Integração Neo (2.0) - COMPLEXO MAS IMPORTANTE
```

---

### 6. **Impact vs Effort Matrix** (Variação do Value vs Effort)
**Uso:** Visualização 2x2 para decisões rápidas

**Igual ao Value vs Effort, mas foca especificamente em:**
- Impact = Efeito na redução de churn / satisfação
- Effort = Recursos necessários

**Exemplo com seus clientes:**

```
HIGH IMPACT, LOW EFFORT (QUICK WINS):
☑ Agendar treinamento AWR (1 dia) → Ativa cliente
☑ Licenças treinamento (2 dias) → Demonstra valor
☑ Puxar agenda Capsicum (1 dia) → Primeiros passos
☑ Templates verticais (2 semanas) → Escopo claro

HIGH IMPACT, HIGH EFFORT (STRATEGIC):
☐ Integração Neo API (4-6 semanas) → Salva Capsicum
☐ Redesenho onboarding (3-4 semanas) → Muda cultura
☐ PLD (6-8 semanas) → Abre novo segmento

LOW IMPACT, LOW EFFORT (FILL-IN):
☐ Ajustes UI
☐ Correções menores

LOW IMPACT, HIGH EFFORT (AVOID):
✗ Redesign gráfico completo
✗ Suporte múltiplos idiomas
```

---

### 7. **Pareto Analysis (80/20 Rule)**
**Uso:** Identificar os 20% de ações que geram 80% do resultado

**Aplicação:**

```
20% DE AÇÕES = 80% DOS RESULTADOS:

1. LIMPEZA AGENDA CAPSICUM + TREINAMENTOS
   → Reduz risco de churn em 40%
   → Timeline: 1-2 semanas
   → Impacto em: Capsicum, AWR, Hike

2. INTEGRAÇÃO NEO API
   → Retém Capsicum + vira diferencial
   → Timeline: 4-6 semanas
   → Impacto: 1 cliente mas churn-preventing

3. REDESENHO ONBOARDING (Parametrização obrigatória)
   → Previne 80% dos problemas futuros
   → Timeline: 3-4 semanas
   → Impacto em: TODOS (presente + futuro)

OUTROS 80% DE AÇÕES (Menos críticas):
- Ajustes UI
- Melhorias secundárias
- Features complementares
- Documentação

CONCLUSÃO: Foque nos 3 acima. Geram 80% do valor.
```

---

### 8. **Design Thinking Framework** (Empatia → Ideação → Prototipagem)
**Uso:** Desenvolver soluções centradas no cliente para quick wins

**Fases:**

```
FASE 1: EMPATIA (O que aprendemos)
✓ Capsicum: Agenda confusa = não usa plataforma, considera migração
✓ AWR: Quer treinar = oportunidade de ativação
✓ Algarve: Compara com IA = insegurança sobre valor
✓ Hike: Desconhece features = precisa educação

FASE 2: DEFINE (O que é o problema real)
Problema Raiz: Falta de parametrização no onboarding deixa clientes confusos
Não é a plataforma que é ruim, é o início que é ruim.

FASE 3: IDEATE (Possíveis soluções)
- Template de onboarding por tipo de cliente
- Checklist de parametrização obrigatória
- Sessão de limpeza assistida
- Dashboard pré-preenchido para primeira login

FASE 4: PROTOTYPE (Teste rápido)
- Criar onboarding parametrizado para Capsicum
- Testar com AWR
- Iterar com feedback

FASE 5: TEST (Validar com cliente)
- Sessão com Capsicum: "Isso funcionaria para você?"
- Feedback → Ajustes → Pronto para 5 clientes

RESULTADO: Solução centrada em cliente, não em produto
```

---

### 9. **Jobs to be Done Framework**
**Uso:** Entender o que cliente realmente quer fazer (seu "job")

**Aplicação:**

```
CAPSICUM:
Job: "Quero fazer compliance de forma simples e rápida"
Current solution: Neo (externo) + upload manual
Desired: Tudo integrado em 1 plataforma

Ação: 
✓ Integração Neo (faz todo workflow em um lugar)
✓ Automatizar (não mais manual)
✓ PLD integrado

---

AWR:
Job: "Quero treinar meu time em compliance sem bagunçar meu dia a dia"
Current solution: Processo manual fora do Compliasset
Desired: Processo integrado no sistema

Ação:
✓ Treinamentos plataforma
✓ Aceites integrados
✓ Agenda limpa (sem ruído)

---

ALGARVE:
Job: "Quero estar certo de estar em compliance sem dúvidas"
Current solution: Comparando com IA/outras plataformas
Desired: Confiança no sistema, validação externa

Ação:
✓ Comparação estruturada com IA
✓ Relatórios mais robustos
✓ Certificações/validações

---

RESULTADO: Você não está vendendo "software", está vendendo "confiança em compliance"
Mude o positioning. Todos querem a mesma coisa = confiança.
```

---

### 10. **Problem Mapping Framework**
**Uso:** Visualizar root causes vs. symptoms

**Exemplo Capsicum:**

```
SYMPTOM: Não usa plataforma, quer migrar
    ↓
SURFACE PROBLEM: Agenda muito poluida
    ↓
DEEPER PROBLEM: Falta limpeza/parametrização no onboarding
    ↓
ROOT CAUSE: Processo de onboarding não inclui etapa de parametrização
    ↓
SYSTEMIC ISSUE: Vendem módulos sem validar fit com cliente

SOLUÇÃO em CASCATA:
1. Imediato: Limpeza retroativa (1-2 semanas)
2. Curto prazo: Integração Neo + PLD (4-8 semanas)
3. Médio prazo: Redesenho onboarding (3-4 semanas mas estrutural)
4. Longo prazo: Mudar processo comercial (validar fit antes de vender)
```

---

## 📊 RESUMO: COMO APLICAR TODOS OS FRAMEWORKS

### Passo 1: Semana 1 - Diagnóstico Rápido
**Frameworks:** Value vs Effort + Eisenhower + RICE
- Identifique as 8 quick wins
- Classifique em urgência
- Score cada ação
- **Output:** Priorizaçao clara

### Passo 2: Semana 2 - Roadmap
**Frameworks:** MoSCoW + Pareto + RICE
- Defina MUST/SHOULD/COULD
- Aplique 80/20: Foque nos 3 itens top
- Crie roadmap Q3 2026
- **Output:** Roadmap claro, timelined

### Passo 3: Semana 2-3 - Implementação Planejada
**Frameworks:** Design Thinking + Jobs to be Done
- Para cada quick win: Empatia → Prototipo
- Entenda o "job" de cada cliente
- Customize soluções
- **Output:** Soluções centradas em cliente

### Passo 4: Semana 3-4 - Acompanhamento
**Frameworks:** Kano + Impact vs Effort + Problem Mapping
- Mapeie satisfiers vs delighters
- Acompanhe impacto cada ação
- Identifique novos problemas root-cause
- **Output:** Iteração contínua

---

## 🎯 EXEMPLO PRÁTICO: Aplicar 3 Frameworks ao Caso Capsicum

### Cenário: "Como salvar Capsicum de churn?"

**Framework 1: Value vs Effort**
```
Quick Win (Fazer já):
- Limpeza agenda (1 semana, muito valor)
- Licenças treinamento (2 dias, demonstra)

Strategic (Planejar):
- Integração Neo (salva cliente, 4-6 semanas)
- PLD (demanda específica, 6-8 semanas)
```

**Framework 2: RICE Scoring**
```
Ranking:
1. Limpeza + Treinamentos (Alto score, baixo effort)
2. Integração Neo (Médio score, alto effort, mas urgente = fazer 2ª)
3. PLD (Médio score, alto effort, 3ª prioridade)
```

**Framework 3: Design Thinking**
```
Empatia: Alice quer simplificar, está pensando em sair
Define: Problema = falta de parametrização no início
Ideate: Limpeza retroativa + onboarding novo
Prototype: Criar limpeza de agenda para Capsicum
Test: "Isso funcionaria para você?"
```

**Resultado:** Claro plano de ação, priorizado, centrado em cliente

---

## 🚀 PRÓXIMOS PASSOS

1. **Aplique RICE** para todas as 8+ ações identificadas
2. **Crie MoSCoW roadmap** com timelines
3. **Use Design Thinking** para estruturar cada quick win
4. **Acompanhe com Pareto** (foque nos 20% top)
5. **Valide com Kano** - converta satisfiers em delighters

---

## 📚 REFERÊNCIAS RÁPIDAS

| Framework | Melhor Para | Resultado |
|-----------|-----------|-----------|
| Value vs Effort | Quick wins | Matriz 2x2 |
| Eisenhower | Urgência | 4 quadrantes |
| MoSCoW | Roadmap | Prioridades claras |
| Kano | Satisfação | Features estratégicas |
| RICE | Scoring | Ranking numérico |
| Impact vs Effort | Decisões | Matriz visual |
| Pareto | 80/20 | Top 3 ações |
| Design Thinking | Soluções | Protótipos |
| Jobs to be Done | Positioning | Customer-centric |
| Problem Mapping | Root cause | Cascata de soluções |

---

**Documento criado:** 08/07/2026  
**Para:** Análise de dados clientes Compliasset  
**Status:** Pronto para aplicação imediata
