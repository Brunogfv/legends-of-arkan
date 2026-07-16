# Resumo do Projeto — Legends of Arkan

Este arquivo contém o resumo executivo do projeto. Leia este documento primeiro ao iniciar
uma nova sessão de IA para obter contexto geral.

---

## Identificação

| Campo            | Valor                           |
|------------------|---------------------------------|
| **Nome**         | Legends of Arkan                |
| **Motor**        | Godot Engine 4.x                |
| **Linguagem**    | GDScript 2.0                    |
| **Gênero**       | *[a definir]*                   |
| **Plataformas**  | Windows, Linux, Web             |
| **Repositório**  | GitHub                          |
| **Licença**      | MIT                             |

---

## Missão do Projeto

Legends of Arkan é um jogo 2D com [gênero a definir] desenvolvido em Godot Engine 4.x.
O projeto segue práticas profissionais de estúdio: documentação completa, pipeline organizado,
controle de versão semântico e sistema de agentes de IA para desenvolvimento assistido.

---

## Estrutura do Repositório

```
Legends-of-Arkan/
├── .ai/              # Sistema de Agentes de IA
├── .github/          # Workflows e templates GitHub
├── assets/           # Assets finais compilados
├── backups/          # Cópias de segurança
├── build/            # Artefatos de build
├── concept_art/      # Arte conceitual
├── docs/             # Documentação completa (20 documentos)
├── exports/          # Builds exportadas
├── game/             # Projeto Godot (código, cenas, recursos)
├── prompts/          # Prompts de IA
├── references/       # Referências visuais e técnicas
├── scripts/          # Scripts de automação
├── source/           # Assets-fonte editáveis
├── tests/            # Testes automatizados
├── tools/            # Ferramentas internas
├── CHANGELOG.md      # Histórico de versões
├── LICENSE           # Licença MIT
└── README.md         # Visão geral
```

---

## Sistema de Agentes

O projeto utiliza 5 agentes de IA especializados que colaboram sequencialmente:

| Agente       | Responsabilidade                  |
|--------------|-----------------------------------|
| Arquiteto    | Estrutura, padrões, decisões técnicas |
| Game Designer| Mecânicas, regras, balanceamento  |
| Desenvolvedor| Implementação de código           |
| QA           | Testes e validação                |
| Revisor      | Revisão de código e documentação  |

---

## Fase Atual

- **Fase:** Concepção
- **Descrição:** Estrutura inicial do projeto e documentação base
- **Início:** 2026-07-16

---

## Próximo Marco

*[a definir]*

---

## Regras Gerais

1. Toda funcionalidade deve ser documentada antes de implementada
2. Código segue padrões definidos em `docs/02_Arquitetura.md`
3. Decisões técnicas são registradas em `templates/decision_template.md`
4. Bugs são documentados em `memory/known_issues.md`
5. O estado do projeto é mantido em `memory/current_state.md`
