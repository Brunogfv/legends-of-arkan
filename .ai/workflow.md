# Workflow de Agentes — Legends of Arkan

Este documento define o fluxo de colaboração entre os agentes de IA do projeto.
Cada tarefa passa por uma sequência definida de agentes antes de ser considerada concluída.

---

## Índice

1. [Visão Geral do Fluxo](#1-visão-geral-do-fluxo)
2. [Fluxo Principal](#2-fluxo-principal)
3. [Fluxo de Correção de Bug](#3-fluxo-de-correção-de-bug)
4. [Fluxo de Decisão Técnica](#4-fluxo-de-decisão-técnica)
5. [Regras de Transição](#5-regras-de-transição)
6. [Handoff entre Agentes](#6-handoff-entre-agentes)

---

## 1. Visão Geral do Fluxo

O desenvolvimento segue uma **cascata flexível** onde cada agente conclui sua etapa
e passa o resultado ao próximo. O fluxo é unidirecional, mas pode haver retorno
em caso de reprovação nas etapas de QA ou Revisão.

```
Arquiteto
    ↓
Game Designer
    ↓
Desenvolvedor
    ↓
QA
    ↓
Revisor
    ↓
Atualização da Documentação
```

---

## 2. Fluxo Principal

### Etapa 1 — Arquiteto

**Entrada:** Requisito ou tarefa definida em `memory/next_task.md`

**Atividades:**
- Analisa o requisito e seu impacto na arquitetura existente
- Define a abordagem técnica, padrões e estruturas
- Documenta a decisão em `docs/02_Arquitetura.md` (se aplicável)
- Atualiza `templates/decision_template.md` com a decisão arquitetural

**Saída:** Especificação técnica clara para o Designer e Desenvolvedor
**Próximo:** Game Designer

---

### Etapa 2 — Game Designer

**Entrada:** Especificação técnica do Arquiteto + requisito original

**Atividades:**
- Define as mecânicas, regras de negócio e comportamento esperado
- Atualiza `docs/` relevantes (GDD, mecânicas, sistemas)
- Cria ou atualiza especificações de design

**Saída:** Especificação de design completa
**Próximo:** Desenvolvedor

---

### Etapa 3 — Desenvolvedor

**Entrada:** Especificação técnica + especificação de design

**Atividades:**
- Implementa o código seguindo os padrões definidos na Arquitetura
- Escreve testes unitários para a funcionalidade
- Segue o template `templates/feature_template.md` para registrar a implementação

**Saída:** Código implementado + testes
**Próximo:** QA

---

### Etapa 4 — QA

**Entrada:** Código implementado + testes + especificação

**Atividades:**
- Executa os testes automatizados
- Realiza testes manuais de regressão
- Verifica se a implementação atende à especificação
- Documenta bugs encontrados em `memory/known_issues.md`

**Saída:** Relatório de QA (aprovado ou reprovado)
**Próximo:** Revisor (se aprovado) | Desenvolvedor (se reprovado)

---

### Etapa 5 — Revisor

**Entrada:** Código aprovado pelo QA + especificações

**Atividades:**
- Revisa qualidade do código (legibilidade, padrões, desempenho)
- Verifica cobertura de testes
- Valida conformidade com a arquitetura
- Sugere melhorias ou aprova

**Saída:** Código revisado (aprovado ou com solicitação de alteração)
**Próximo:** Documentação (se aprovado) | Desenvolvedor (se solicitado alteração)

---

### Etapa 6 — Atualização da Documentação

**Entrada:** Funcionalidade concluída e revisada

**Atividades:**
- Atualiza `memory/completed_features.md` com a nova funcionalidade
- Atualiza `memory/current_state.md` com o novo estado
- Atualiza `memory/next_task.md` com a próxima tarefa
- Se houver bugs conhecidos, mantém `memory/known_issues.md` atualizado

**Saída:** Memória do projeto atualizada

---

## 3. Fluxo de Correção de Bug

```
QA ou Usuário reporta bug
    ↓
Bug registrado em memory/known_issues.md com template bug_template.md
    ↓
Arquiteto avalia impacto
    ↓
Desenvolvedor implementa correção
    ↓
QA valida correção
    ↓
Revisor aprova
    ↓
Documentação atualizada
```

---

## 4. Fluxo de Decisão Técnica

```
Necessidade de decisão identificada
    ↓
Arquiteto cria entrada em templates/decision_template.md
    ↓
Decisão documentada com justificativa e alternativas
    ↓
Revisor valida a decisão
    ↓
Documentação atualizada (docs/02_Arquitetura.md se necessário)
```

---

## 5. Regras de Transição

1. **Cada etapa deve ser concluída antes de passar para a próxima.**
2. **Se uma etapa for reprovada, a tarefa retorna ao agente anterior.**
3. **O handoff deve incluir um resumo do que foi feito e o que espera do próximo agente.**
4. **Nenhum agente pode pular etapas.**
5. **Em caso de tarefa puramente documental, os agentes técnicos (Desenvolvedor, QA) podem ser ignorados.**

---

## 6. Handoff entre Agentes

Ao passar uma tarefa para o próximo agente, inclua:

```markdown
## Handoff

**Agente Origem:** [nome do agente]
**Agente Destino:** [nome do agente]
**Tarefa:** [descrição sucinta]
**O que foi feito:** [resumo]
**O que esperar:** [orientações]
**Arquivos modificados:** [lista]
**Arquivos a modificar:** [lista]
**Observações:** [notas importantes]
```
