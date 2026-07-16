# Arquitetura — Legends of Arkan

| Campo             | Valor                              |
|-------------------|------------------------------------|
| **Nome**          | Arquitetura do Projeto             |
| **Objetivo**      | Documentar a arquitetura técnica, padrões de código e organização do motor |
| **Versão**        | 0.1.0                              |
| **Data**          | 2026-07-16                         |
| **Autor**         | Arquiteto de Software              |

---

## Índice

1. [Stack Tecnológica](#1-stack-tecnológica)
2. [Arquitetura do Godot](#2-arquitetura-do-godot)
3. [Padrões de Projeto](#3-padrões-de-projeto)
4. [Organização de Cenas](#4-organização-de-cenas)
5. [Hierarquia de Autoloads](#5-hierarquia-de-autoloads)
6. [Sistemas e Serviços](#6-sistemas-e-serviços)
7. [Pipeline de Assets](#7-pipeline-de-assets)
8. [Documentos Relacionados](#8-documentos-relacionados)

---

## 1. Stack Tecnológica

- **Motor:** Godot Engine 4.x
- **Linguagem:** GDScript 2.0
- **Versionamento:** Git + GitHub
- **Arte:** Aseprite / Krita
- **Áudio:** Audacity / Bosca Ceoil
- **Mapas:** Tiled / Ferramenta interna

---

## 2. Arquitetura do Godot

*[A ser preenchido — árvore de cenas, estrutura de nós principal, GameManager, etc.]*

### Padrão de Organização

```
res://
├── core/           # Scripts base, managers, singletons
├── entities/       # Player, NPCs, inimigos
├── systems/        # Combate, inventário, crafting, economia
├── ui/             # HUD, menus, inventário
├── world/          # Mapas, tilesets, cenários
├── items/          # Definições de itens, receitas
└── data/           # Recursos, bases de dados, configurações
```

---

## 3. Padrões de Projeto

- **Singleton (Autoload):** GameManager, AudioManager, DataManager
- **State Machine:** Entidades (Player, Inimigos)
- **Observer (Signals):** Eventos de combate, missões, UI
- **Factory:** Geração de itens, inimigos, projéteis
- **Command:** Input handling, ações do jogador
- **Resource:** Definições de dados via Godot Resources

---

## 4. Organização de Cenas

*[A ser preenchido — estrutura de cenas: Game, UI, Menus, Levels.]*

---

## 5. Hierarquia de Autoloads

```
GameManager (singleton)
├── DataManager
├── AudioManager
├── EventBus
├── SaveManager
├── SceneManager
└── InputManager
```

---

## 6. Sistemas e Serviços

| Sistema         | Descrição                          | Autoload  |
|-----------------|------------------------------------|-----------|
| GameManager     | Estado global, ciclo de jogo       | Sim       |
| DataManager     | Banco de dados, configurações      | Sim       |
| AudioManager    | Áudio e música                     | Sim       |
| EventBus        | Sistema de eventos globais         | Sim       |
| CombatSystem    | Lógica de combate                  | Não       |
| InventorySystem | Gerenciamento de inventário        | Não       |
| CraftingSystem  | Sistema de crafting                | Não       |

---

## 7. Pipeline de Assets

```
source/ (editável)
    ↓ Exportação
assets/ (final)
    ↓ Importação Godot
game/ (uso no motor)
```

---

## 8. Documentos Relacionados

- `docs/00_Documento_Mestre.md`
- `docs/04_Manual_Tecnico.md`
- `docs/12_Sistema_Combate.md`
- `docs/13_Sistema_Inventario.md`
- `docs/14_Sistema_Crafting.md`
- `docs/16_IA.md`

---

## Histórico de Alterações

| Versão | Data       | Descrição                     | Autor                |
|--------|------------|-------------------------------|----------------------|
| 0.1.0  | 2026-07-16 | Criação inicial do documento  | Arquiteto de Software |
