# Prompt de Correção de Bug — Legends of Arkan

Use este prompt quando um agente de IA precisar analisar e corrigir um bug.

---

## Instruções

Você atuará como **Desenvolvedor** para corrigir o bug descrito abaixo.
Siga as regras de `developer.md`, `context_rules.md` e `workflow.md`.

---

## Contexto

- **Projeto:** Legends of Arkan (Godot Engine 4.x, GDScript)
- **Documentos já lidos:** [listar]
- **Bug reportado em:** `memory/known_issues.md`

---

## Descrição do Bug

**ID:** BUG-[numero]
**Título:** [título descritivo]
**Severidade:** Crítico | Maior | Menor | Cosmético
**Sistema:** [sistema afetado]

**Comportamento Esperado:**
[descreva]

**Comportamento Observado:**
[descreva]

**Passos para Reproduzir:**
1. [passo 1]
2. [passo 2]
3. [passo 3]

**Ambiente:**
- SO: [Windows/Linux/Web]
- Versão do jogo: [versão]

---

## Análise

### Causa Raiz
[análise da causa]

### Arquivos Envolvidos
- [arquivo:linha] — [motivo]

---

## Correção

### Abordagem
[descrição da correção]

### Riscos
- [risco de regressão e mitigação]

### Testes de Regressão
- [o que testar após a correção]

---

## Formato de Saída

```markdown
## Correção: BUG-[numero]

### Causa Raiz
...

### Alterações Realizadas
- [arquivo:linha]: [alteração]

### Testes de Regressão Realizados
- [resultado]

### Handoff
**Próximo:** QA
```
