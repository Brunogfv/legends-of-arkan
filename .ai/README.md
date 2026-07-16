# Sistema de Agentes de IA — Legends of Arkan

Este diretório contém a infraestrutura de agentes de IA do projeto **Legends of Arkan**.
O sistema é independente de ferramenta (OpenCode, Cursor, Claude Code, Codex, Gemini CLI, etc.)
e foi projetado para garantir consistência, rastreabilidade e escalabilidade durante todo o desenvolvimento.

---

## Estrutura

```
.ai/
├── README.md            # Este arquivo
├── workflow.md          # Fluxo de colaboração entre agentes
├── context_rules.md     # Regras de recuperação de contexto
├── architect.md         # Agente: Arquiteto de Software
├── developer.md         # Agente: Desenvolvedor
├── designer.md          # Agente: Game Designer
├── qa.md                # Agente: QA / Testes
├── reviewer.md          # Agente: Revisor de Código
├── prompts/             # Prompts especializados por tarefa
│   ├── planning.md
│   ├── implementation.md
│   ├── review.md
│   ├── bugfix.md
│   └── refactor.md
├── templates/           # Templates reutilizáveis
│   ├── feature_template.md
│   ├── decision_template.md
│   ├── bug_template.md
│   └── system_template.md
└── memory/              # Memória persistente do projeto
    ├── current_state.md
    ├── next_task.md
    ├── project_summary.md
    ├── known_issues.md
    └── completed_features.md
```

---

## Como Usar

1. Leia `context_rules.md` para entender como carregar o contexto.
2. Consulte `memory/current_state.md` para saber o estado atual.
3. Siga `workflow.md` para saber qual agente deve atuar.
4. Use os prompts em `prompts/` para tarefas específicas.
5. Use os templates em `templates/` para criar documentação padronizada.
6. Atualize `memory/` ao concluir cada tarefa.

---

## Agentes

| Agente         | Arquivo          | Responsabilidade Principal               |
|----------------|------------------|------------------------------------------|
| Arquiteto      | `architect.md`   | Estrutura, padrões, decisões técnicas    |
| Desenvolvedor  | `developer.md`   | Implementação de código                  |
| Game Designer  | `designer.md`    | Design de jogabilidade e sistemas        |
| QA             | `qa.md`          | Testes e validação de qualidade          |
| Revisor        | `reviewer.md`    | Revisão de código e documentação         |

---

## Princípios

- **Rastreabilidade:** Toda decisão é documentada em `templates/decision_template.md`.
- **Consistência:** Todos os agentes seguem os mesmos padrões e templates.
- **Memória Persistente:** O diretório `memory/` é a fonte de verdade do estado do projeto.
- **Independente de Ferramenta:** O sistema funciona com qualquer assistente de IA.
