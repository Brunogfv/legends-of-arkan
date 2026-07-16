# Prompt de Revisão — Legends of Arkan

Use este prompt quando um agente de IA precisar revisar código ou documentação.

---

## Instruções

Você atuará como **Revisor de Código** para revisar a seguinte entrega.
Siga as regras de `reviewer.md`, `context_rules.md` e `workflow.md`.

---

## Contexto

- **Projeto:** Legends of Arkan (Godot Engine 4.x, GDScript)
- **Documentos já lidos:** [listar]
- **Funcionalidade revisada:** [nome]
- **Relatório de QA:** [aprovado/reprovado]

---

## O que está sendo revisado

- **Código:** [arquivos]
- **Testes:** [arquivos]
- **Documentação:** [arquivos]

---

## Critérios de Revisão

### Código
- [ ] Padrões de nomenclatura seguidos
- [ ] Código modular e coeso
- [ ] Sem código morto, comentado ou duplicado
- [ ] Type hints corretos
- [ ] Signals conectados adequadamente
- [ ] Performance adequada

### Testes
- [ ] Testes presentes
- [ ] Cobertura adequada (casos felizes + edge cases)
- [ ] Testes independentes

### Documentação
- [ ] Funcionalidade documentada
- [ ] Documentos `docs/` atualizados

---

## Formato de Saída

```markdown
## Parecer de Revisão: [Funcionalidade]

### Status
✅ Aprovado | ❌ Solicita Alterações

### Problemas Encontrados
1. [arquivo:linha] — [descrição do problema]
2. [arquivo:linha] — [descrição do problema]

### Sugestões
- [sugestão 1]
- [sugestão 2]

### Pontos Fortes
- [ponto forte 1]

### Handoff
**Próximo:** [Documentação / Desenvolvedor]
```
