# Documento Mestre — Legends of Arkan

| Campo             | Valor                    |
|-------------------|--------------------------|
| **Nome**          | Documento Mestre         |
| **Objetivo**      | Centralizar e governar toda a documentação do projeto |
| **Versão**        | 0.1.0                    |
| **Data**          | 2026-07-16               |
| **Autor**         | Equipe Legends of Arkan  |

---

## Índice

1. [Visão Geral](#1-visão-geral)
2. [Estrutura Documental](#2-estrutura-documental)
3. [Convenções](#3-convenções)
4. [Glossário](#4-glossário)
5. [Documentos Relacionados](#5-documentos-relacionados)

---

## 1. Visão Geral

Legends of Arkan é um jogo 2D desenvolvido em Godot Engine 4.x. Este documento governa todos os demais documentos do projeto, definindo padrões, convenções e a hierarquia documental.

---

## 2. Estrutura Documental

### Documentos Principais

| #   | Documento                               | Responsável    |
|-----|-----------------------------------------|----------------|
| 00  | Documento Mestre                        | Arquiteto      |
| 01  | Game Design Document (GDD)              | Game Designer  |
| 02  | Arquitetura                             | Arquiteto      |
| 03  | Diário de Desenvolvimento               | Toda Equipe    |
| 04  | Manual Técnico                          | Tech Lead      |

### Documentos de Design

| #   | Documento                               | Responsável    |
|-----|-----------------------------------------|----------------|
| 05  | Lore                                    | Roteirista     |
| 06  | Mecânicas                               | Game Designer  |
| 07  | NPCs                                    | Game Designer  |
| 08  | Monstros                                | Game Designer  |
| 09  | Itens                                   | Game Designer  |
| 10  | Mapas                                   | Level Designer |
| 11  | Missões                                 | Game Designer  |

### Documentos de Sistemas

| #   | Documento                               | Responsável    |
|-----|-----------------------------------------|----------------|
| 12  | Sistema de Combate                      | Programador    |
| 13  | Sistema de Inventário                   | Programador    |
| 14  | Sistema de Crafting                     | Programador    |
| 15  | Economia                                | Game Designer  |
| 16  | IA                                      | Programador    |

### Documentos de Produção

| #   | Documento                               | Responsável    |
|-----|-----------------------------------------|----------------|
| 17  | Arte                                    | Art Lead       |
| 18  | Áudio                                   | Audio Lead     |
| 19  | Publicação                              | Produtor       |

---

## 3. Convenções

### Nomenclatura de Arquivos

- Diretórios: `snake_case`
- Documentos: `NN_Nome_Descritivo.md` (NN = número sequencial de dois dígitos)
- Assets: `tipo_subtipo_descricao_v01.png`
- Scripts: `snake_case.gd`

### Versionamento

O projeto segue **Semantic Versioning** (MAJOR.MINOR.PATCH).

### Commits

Padrão **Conventional Commits**:
- `feat:` — Nova funcionalidade
- `fix:` — Correção de bug
- `docs:` — Documentação
- `refactor:` — Refatoração
- `test:` — Testes
- `chore:` — Manutenção

---

## 4. Glossário

| Termo           | Definição                                      |
|-----------------|------------------------------------------------|
| GDD             | Game Design Document                           |
| Tick            | Ciclo principal do jogo (process frame)        |
| Asset           | Recurso utilizado no jogo (sprite, áudio, etc) |
| Scene           | Cena do Godot (organização de nós)             |
| Node            | Elemento base da árvore de cenas do Godot      |
| Signal          | Sistema de eventos do Godot                    |

---

## 5. Documentos Relacionados

- Todos os documentos listados na seção 2.
- `README.md` — Visão geral do repositório
- `CHANGELOG.md` — Histórico de versões

---

## Histórico de Alterações

| Versão | Data       | Descrição                   | Autor            |
|--------|------------|-----------------------------|------------------|
| 0.1.0  | 2026-07-16 | Criação inicial do documento | Equipe do Projeto |
