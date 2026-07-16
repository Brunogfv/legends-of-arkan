# Legends of Arkan

Bem-vindo ao repositório oficial de **Legends of Arkan** — um jogo 2D desenvolvido com **Godot Engine 4.x**.

---

## Sobre o Projeto

Legends of Arkan é um [gênero a definir] com atmosfera rica, combate dinâmico e progressão baseada em exploração e crafting. O projeto é desenvolvido seguindo práticas profissionais de estúdio, com documentação completa, pipeline de assets organizado e versionamento semântico.

---

## Estrutura do Projeto

```
Legends-of-Arkan/
├── .github/           # Workflows, templates e configurações GitHub
├── assets/            # Assets finais (.png, .ogg, .tscn, .glb, etc.)
├── backups/           # Cópias de segurança do projeto
├── build/             # Artefatos de build (intermediários)
├── concept_art/       # Arte conceitual e referências visuais
├── docs/              # Documentação completa do jogo
│   ├── 00_Documento_Mestre.md
│   ├── 01_Game_Design_Document.md
│   ├── 02_Arquitetura.md
│   ├── 03_Diario_Desenvolvimento.md
│   ├── 04_Manual_Tecnico.md
│   ├── 05_Lore.md
│   ├── 06_Mecanicas.md
│   ├── 07_NPCs.md
│   ├── 08_Monstros.md
│   ├── 09_Itens.md
│   ├── 10_Mapas.md
│   ├── 11_Missoes.md
│   ├── 12_Sistema_Combate.md
│   ├── 13_Sistema_Inventario.md
│   ├── 14_Sistema_Crafting.md
│   ├── 15_Economia.md
│   ├── 16_IA.md
│   ├── 17_Arte.md
│   ├── 18_Audio.md
│   └── 19_Publicacao.md
├── exports/           # Builds finais exportadas (Windows, Linux, Web, etc.)
├── game/              # Projeto Godot (project.godot, cenas, scripts)
├── prompts/           # Prompts de IA e documentação de assistência
├── references/        # Materiais de referência (tutoriais, spritesheets)
├── scripts/           # Scripts auxiliares (automação, build, deploy)
├── source/            # Assets-fonte editáveis (.psd, .kra, .blend, etc.)
├── tests/             # Testes automatizados (GDScript Unit Tests)
├── tools/             # Ferramentas internas (editores de mapa, diálogo)
├── CHANGELOG.md       # Histórico de versões
├── LICENSE            # Licença MIT
└── README.md          # Este arquivo
```

---

## Diretórios Detalhados

### `game/`
Projeto principal do Godot Engine. Contém `project.godot`, todas as cenas (`*.tscn`), scripts (`*.gd`), recursos (`*.tres`, `*.res`) e configurações de importação.

### `docs/`
Documentação completa do projeto, desde o Documento Mestre até especificações técnicas de sistemas, arte e áudio. Cada documento segue um padrão profissional com cabeçalho, índice e histórico de alterações.

### `assets/`
Assets finais compilados e prontos para uso no motor. Organizados por tipo:
- `assets/sprites/` — Sprites e tilesets
- `assets/ui/` — Interface do usuário
- `assets/audio/` — Efeitos sonoros e música
- `assets/animations/` — Animações
- `assets/fonts/` — Fontes tipográficas
- `assets/shaders/` — Shaders personalizados
- `assets/particles/` — Sistemas de partículas
- `assets/3d/` — Modelos 3D (se aplicável)

### `source/`
Arquivos-fonte editáveis dos assets (Photoshop, Krita, Blender, etc.). Mantidos separados dos assets finais para preservar o pipeline de produção.

### `concept_art/`
Arte conceitual, estudos de personagens, cenários e storyboards.

### `references/`
Referências visuais, técnicas e de design coletadas durante o desenvolvimento.

### `scripts/`
Scripts de automação para pipeline de assets, build, deploy e tarefas de desenvolvimento.

### `tools/`
Ferramentas internas personalizadas: editores de mapa, diálogo, balanceamento, etc.

### `tests/`
Testes unitários e de integração para sistemas do jogo, escritos em GDScript utilizando a estrutura de testes do Godot.

### `build/`
Artefatos intermediários de build (não versionados).

### `exports/`
Builds finais exportadas do jogo para distribuição (não versionados).

### `backups/`
Cópias de segurança do projeto (não versionados).

### `.github/`
Templates de issues, pull requests e workflows de CI/CD.

---

## Tecnologias

| Tecnologia    | Versão |
|---------------|--------|
| Godot Engine  | 4.x    |
| GDScript      | 2.0    |
| Git           | 2.x    |

---

## Como Contribuir

1. Leia a documentação em `docs/` para entender a visão do projeto.
2. Consulte o `docs/03_Diario_Desenvolvimento.md` para tarefas em andamento.
3. Siga o padrão de branching: `main` → `dev` → `feature/<nome>`.
4. Commits devem seguir [Conventional Commits](https://www.conventionalcommits.org/).
5. Pull requests devem ser revisados e vinculados a uma issue.

---

## Licença

Este projeto está licenciado sob a [MIT License](LICENSE).
