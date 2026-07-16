# Índice de Decisões — Frozen Decisions

Este documento lista **todas as decisões registradas** do projeto Legends of Arkan.
Consulte-o para navegar pelo histórico de decisões ou para verificar se uma decisão
já foi tomada antes de criar uma nova.

---

## Índice de Decisões

| ID | Nome | Status | Data | Documentos Relacionados |
|----|------|--------|------|------------------------|
| DEC-001 | Visão do Jogo | Aprovada | 2026-07-16 | `DESIGN_COMPASS.md`, `docs/01_GDD.md` |
| DEC-002 | Fantasia do Jogador | Aprovada | 2026-07-16 | `DESIGN_COMPASS.md`, `docs/05_Lore.md` |
| DEC-003 | Pilares de Design | Aprovada | 2026-07-16 | `DESIGN_COMPASS.md`, `docs/01_GDD.md`, `docs/06_Mecanicas.md` |

---

## Status e Significado

| Status | Significado |
|--------|-------------|
| **Proposta** | Decisão sugerida, aguardando discussão |
| **Em discussão** | Em análise, prós e contras sendo avaliados |
| **Aprovada** | Decisão finalizada e vigente |
| **Substituída** | Uma nova decisão substituiu esta (ver campo "Substituída por") |
| **Obsoleta** | Não é mais aplicável (contexto mudou, sistema foi removido, etc.) |

---

## Regras do Sistema

### Identificador Único

Toda decisão recebe um ID sequencial no formato `DEC-NNN`.

| Faixa | Tipo de Decisão |
|-------|-----------------|
| DEC-001 a DEC-099 | Decisões de game design e visão |
| DEC-100 a DEC-199 | Decisões arquiteturais e técnicas |
| DEC-200 a DEC-299 | Decisões de sistema e mecânicas |
| DEC-300 a DEC-399 | Decisões de produção e processo |
| DEC-400+ | Expansões futuras |

### Imutabilidade

**Nenhuma decisão aprovada pode ser alterada diretamente.**

Se uma decisão precisa ser modificada:
1. Crie uma nova decisão usando o `DECISION_TEMPLATE.md`.
2. No campo **Substitui**, referencie a decisão anterior.
3. Atualize a decisão anterior com o campo **Substituída por** apontando para a nova.
4. A nova decisão entra em vigor; a anterior permanece como registro histórico.

### Rastreabilidade

Toda decisão deve referenciar:
- Os documentos de design ou arquitetura que a motivaram.
- Os sistemas do jogo que serão afetados.
- A(s) decisão(ões) que substitui (se aplicável).

### Quando Registrar uma Decisão

Registre uma decisão quando:

- [ ] Uma direção de design significativa é definida.
- [ ] Uma alternativa técnica relevante é escolhida.
- [ ] Um pilar de design é criado, modificado ou removido.
- [ ] Uma funcionalidade tem seu escopo alterado de forma significativa.
- [ ] Um sistema é adicionado, removido ou substituído.
- [ ] Um padrão arquitetural é definido ou alterado.
- [ ] Uma tecnologia ou ferramenta é escolhida em detrimento de outra.
- [ ] Um risco identificado gera uma mudança de abordagem.

### Checklist para Criar uma Nova Decisão

- [ ] ID único e sequencial atribuído
- [ ] Template `DECISION_TEMPLATE.md` preenchido
- [ ] Contexto e problema claramente definidos
- [ ] Pelo menos 2 opções consideradas (quando aplicável)
- [ ] Justificativa técnica ou de design registrada
- [ ] Impactos positivos e negativos listados
- [ ] Riscos identificados e mitigados
- [ ] Documentos relacionados referenciados
- [ ] Sistemas afetados listados
- [ ] Índice `000_DECISION_INDEX.md` atualizado com a nova entrada
- [ ] Se substitui uma decisão anterior, campos de substituição preenchidos em ambas

---

## Como Criar uma Nova Decisão

1. Copie `DECISION_TEMPLATE.md` para `decisions/DEC-NNN_Nome_Da_Decisao.md`.
2. Preencha todos os campos obrigatórios.
3. Adicione a entrada na tabela deste índice.
4. Se a decisão substitui uma anterior, atualize os campos de referência em ambas.
5. Faça commit da nova decisão junto com a atualização do índice.

---

## Histórico de Alterações

| Versão | Data | Descrição | Autor |
|--------|------|-----------|-------|
| 1.0 | 2026-07-16 | Criação inicial do índice | Arquiteto-Chefe |
