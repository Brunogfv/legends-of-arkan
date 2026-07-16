# Prompt de Refatoração — Legends of Arkan

Use este prompt quando um agente de IA precisar refatorar código existente
sem alterar comportamento externo.

---

## Instruções

Você atuará como **Desenvolvedor** para refatorar o código descrito abaixo.
Siga as regras de `developer.md`, `context_rules.md` e `workflow.md`.

---

## Contexto

- **Projeto:** Legends of Arkan (Godot Engine 4.x, GDScript)
- **Documentos já lidos:** [listar]
- **Sistema alvo:** [sistema a refatorar]

---

## Objetivo da Refatoração

- [ ] Melhorar legibilidade
- [ ] Reduzir acoplamento
- [ ] Aumentar coesão
- [ ] Extrair responsabilidades
- [ ] Renomear para clareza
- [ ] Otimizar performance
- [ ] Remover código morto
- [ ] Alinhar com padrões arquiteturais

---

## Escopo

### Arquivos envolvidos
- [arquivo] — [escopo da refatoração]

### Dependências
- [sistemas que dependem deste código]
- [testes existentes]

---

## Abordagem

1. **Análise:** [entender o código atual]
2. **Estrutura alvo:** [como ficará após refatoração]
3. **Preservação de comportamento:** [garantir que nada muda externamente]
4. **Testes:** [verificar que testes existentes continuam passando]

---

## Riscos

- [risco e estratégia de mitigação]

---

## Formato de Saída

```markdown
## Refatoração: [Sistema]

### Motivação
...

### Mudanças Realizadas
- [arquivo]: [resumo da mudança]

### Comportamento Preservado
- [comportamento verificado]

### Testes
- Testes existentes: ✅ passando
- Novos testes: [quantidade]

### Handoff
**Próximo:** QA
```
