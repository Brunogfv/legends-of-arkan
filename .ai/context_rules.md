# Regras de Contexto — Legends of Arkan

Este documento define como qualquer agente de IA deve recuperar e utilizar o contexto do projeto
antes de iniciar uma tarefa. Siga estas regras rigorosamente para evitar alterações fora de escopo,
retrabalho e inconsistências.

---

## Índice

1. [Carga Inicial de Contexto](#1-carga-inicial-de-contexto)
2. [Hierarquia de Leitura](#2-hierarquia-de-leitura)
3. [Identificação da Fase Atual](#3-identificação-da-fase-atual)
4. [Escopo de Alteração](#4-escopo-de-alteração)
5. [Regras de Ouro](#5-regras-de-ouro)

---

## 1. Carga Inicial de Contexto

Sempre que uma sessão de IA for iniciada, o agente DEVE carregar os seguintes documentos
nesta ordem:

### Passo 1 — Visão Geral do Projeto
```
Leia: .ai/memory/project_summary.md
Motivo: Obter resumo executivo do projeto, propósito e regras gerais.
```

### Passo 2 — Estado e Próxima Tarefa
```
Leia: .ai/memory/current_state.md
Leia: .ai/memory/next_task.md
Motivo: Saber o que está sendo feito agora e o que vem a seguir.
```

### Passo 3 — Regras de Contexto e Workflow
```
Leia: .ai/context_rules.md (este arquivo)
Leia: .ai/workflow.md
Motivo: Entender como os agentes colaboram e quais regras seguir.
```

### Passo 4 — Agente Específico
```
Leia: .ai/<seu_agente>.md (ex: architect.md, developer.md)
Motivo: Conhecer sua missão, limites e fluxo de trabalho.
```

### Passo 5 — Documentação do Projeto
```
Consulte os documentos em docs/ conforme necessidade da tarefa.
Prioridade:
  1. docs/00_Documento_Mestre.md
  2. docs/02_Arquitetura.md (se tarefa técnica)
  3. docs/01_Game_Design_Document.md (se tarefa de design)
  4. docs relevantes ao sistema sendo modificado
```

### Passo 6 — Problemas Conhecidos
```
Leia: .ai/memory/known_issues.md
Motivo: Evitar reintroduzir bugs ou problemas já documentados.
```

---

## 2. Hierarquia de Leitura

A leitura deve seguir esta prioridade decrescente:

| Prioridade | O que ler                                           | Motivo                              |
|------------|-----------------------------------------------------|-------------------------------------|
| 1          | `.ai/memory/project_summary.md`                     | Resumo executivo                    |
| 2          | `.ai/memory/current_state.md`                       | Estado atual do projeto             |
| 3          | `.ai/memory/next_task.md`                           | Próxima tarefa                       |
| 4          | `.ai/context_rules.md`                              | Regras de contexto                  |
| 5          | `.ai/workflow.md`                                   | Fluxo de colaboração                |
| 6          | `.ai/<agente>.md`                                   | Definição do agente atual           |
| 7          | `.ai/memory/known_issues.md`                        | Problemas conhecidos                |
| 8          | `docs/` relevantes                                  | Documentação do projeto             |

---

## 3. Identificação da Fase Atual

A fase atual do projeto está sempre definida em:

- `.ai/memory/current_state.md` — Campo `Fase Atual`

### Fases Possíveis

| Fase         | Descrição                                      |
|--------------|------------------------------------------------|
| Concepção    | Definição de escopo, GDD, regras de negócio    |
| Prototipação | MVP, prova de conceito, core loop funcional    |
| Produção     | Implementação completa de sistemas e conteúdo  |
| Polimento    | Refinamento, otimização, correção de bugs      |
| Lançamento   | Build final, publicação, marketing             |
| Pós-Lançamento | Suporte, patches, conteúdo novo              |

Nenhuma tarefa deve ser iniciada sem que a fase atual esteja clara.

---

## 4. Escopo de Alteração

### Regras de Alteração

1. **Nunca modifique arquivos fora do escopo do seu agente.** Consulte `.ai/<seu_agente>.md` para saber quais arquivos pode modificar.
2. **Nunca implemente funcionalidades não documentadas.** Toda funcionalidade deve estar especificada em `docs/` antes de ser implementada.
3. **Nunca pule o fluxo de trabalho.** A sequência Arquiteto → Designer → Desenvolvedor → QA → Revisor → Documentação deve ser respeitada.
4. **Nunca ignore a memória do projeto.** Sempre verifique `memory/` antes de agir.

### O que NÃO fazer

- ⛔ Implementar código sem especificação
- ⛔ Modificar arquivos de agente sem permissão explícita
- ⛔ Ignorar problemas listados em `known_issues.md`
- ⛔ Avançar para a próxima tarefa sem atualizar a memória

---

## 5. Regras de Ouro

1. **Contexto primeiro, código depois.** Sempre carregue o contexto antes de escrever qualquer linha.
2. **Documente antes de implementar.** Primeiro registre a decisão em `docs/`, depois codifique.
3. **Um agente por vez.** Cada tareja é executada por um único agente por vez.
4. **Memória sempre atualizada.** Ao concluir uma tarefa, atualize `memory/current_state.md`, `memory/completed_features.md` e `memory/next_task.md`.
5. **Problemas são documentados imediatamente.** Bugs conhecidos vão para `memory/known_issues.md` assim que identificados.
