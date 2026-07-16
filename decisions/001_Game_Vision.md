# DEC-001 — Visão do Jogo

---

## Metadados

| Campo | Valor |
|-------|-------|
| **ID** | DEC-001 |
| **Título** | Visão do Jogo — RPG Sistêmico Focado em Exploração, Mundo Vivo e Consequências |
| **Data** | 2026-07-16 |
| **Autor** | Diretor Criativo / Lead Game Designer |
| **Status** | Aprovada |
| **Substitui** | — |
| **Substituída por** | — |

---

## Contexto

Durante a fase de concepção do projeto, foi necessário definir a identidade central de Legends of Arkan. Sem uma visão clara, o risco de scope creep e inconsistência de design seria alto. As principais influências consideradas incluíram jogos como Stardew Valley (sistemas interconectados), Terraria (exploração e ferramentas), Dead Cells (combate ágil) e Moonlighter (economia e risco/recompensa).

O projeto precisava de uma direção que:
- Diferenciasse o jogo no mercado de jogos 2D.
- Fosse viável para um desenvolvedor solo assistido por IA.
- Oferecesse profundidade sem exigir recursos de um estúdio AAA.
- Permitisse crescimento incremental (MVP → Alpha → Beta → Release).

---

## Problema

Qual é a identidade central de Legends of Arkan? Que experiência única o jogo oferece que justifica sua existência? Sem esta definição, cada sistema seria projetado isoladamente, resultando em um jogo sem coesão.

---

## Objetivo

Definir a visão do jogo de forma clara o suficiente para que toda decisão futura de design, arte, áudio e programação possa ser avaliada contra ela. A visão deve ser específica o bastante para guiar, mas flexível o bastante para permitir criatividade.

---

## Opções Consideradas

### Opção A: RPG Sistêmico com Exploração, Mundo Vivo e Consequências

**Descrição:** Um jogo onde sistemas interagem para gerar experiências emergentes. O foco não está em uma história roteirizada, mas em um mundo que reage às ações do jogador. Exploração é a atividade central — cada área contém descobertas, não apenas obstáculos. O mundo funciona com ou sem o jogador.

**Prós:**
- Diferenciação no mercado de jogos 2D.
- Rejogabilidade natural (cada partida gera histórias diferentes).
- Sistemas podem ser construídos incrementalmente.
- Profundidade sem exigir produção cara de conteúdo roteirizado.

**Contras:**
- Exige design cuidadoso para que sistemas sejam interessantes.
- Mundo vivo tem custo de implementação maior que mundo estático.
- Mais complexo de testar (sistemas interagem de formas imprevisíveis).

---

### Opção B: Ação Linear com História Roteirizada

**Descrição:** Um jogo focado em combate ágil com fases lineares, chefes e uma história principal forte. Similar a jogos como Shovel Knight ou Hollow Knight (estrutura de progressão, não o gênero).

**Prós:**
- Mais previsível de implementar.
- História pode ser mais impactante (roteirizada).
- Menos risco de sistemas falharem.

**Contras:**
- Menor rejogabilidade.
- Mercado mais saturado.
- Depende fortemente de conteúdo produzido (cenários, animações, diálogos).
- Menos alinhado com a proposta de "mundo que reage ao jogador".

---

### Opção C: Survival Crafting Genérico

**Descrição:** Seguir a fórmula de jogos de sobrevivência com crafting, construção de base e gerenciamento de recursos.

**Prós:**
- Gênero popular com público consolidado.
- Mecânicas bem estabelecidas.

**Contras:**
- Mercado extremamente saturado.
- Exigiria foco em construção/base, que não é o objetivo do projeto.
- Difícil diferenciar-se de títulos estabelecidos.
- Menos alinhado com o objetivo de portfólio (demonstrar design sistêmico).

---

## Alternativa Escolhida

**Decisão:** Opção A — RPG Sistêmico com Exploração, Mundo Vivo e Consequências.

---

## Justificativa Técnica

A Opção A foi escolhida por três razões principais:

1. **Viabilidade para desenvolvedor solo:** Sistemas interconectados podem ser construídos um de cada vez (MVP). Diferente de uma campanha roteirizada (que exige grande produção de conteúdo de uma vez), sistemas podem ser adicionados incrementalmente.

2. **Diferenciação e portfólio:** Um jogo sistêmico demonstra habilidades mais avançadas de arquitetura de software, design de sistemas e balanceamento. É um portfólio mais forte que um jogo linear genérico.

3. **Alinhamento com Design Compass:** A visão escolhida é a única que suporta os quatro pilares (Exploração, Mundo Vivo, Consequências, Progressão) de forma equilibrada. As outras opções favoreceriam apenas um ou dois pilares.

---

## Impactos Positivos

- Diferenciação clara no mercado.
- Base para histórias emergentes (rejogabilidade).
- Estrutura de desenvolvimento incremental viável.
- Portfólio técnico mais forte.
- Decisões de design têm um "norte" claro.

---

## Impactos Negativos

- Maior complexidade de implementação que um jogo linear.
- Risco de sistemas interagirem de formas não intencionais.
- Exige documentação mais rigorosa para manter consistência.

---

## Riscos

| Risco | Probabilidade | Impacto | Mitigação |
|-------|:------------:|:-------:|-----------|
| Sistemas muito complexos para desenvolvedor solo | Média | Alto | MVP enxuto, adicionar complexidade incrementalmente |
| Dificuldade de balancear sistemas interconectados | Alta | Médio | Testes frequentes, playtests desde o MVP |
| Mundo vivo pode não ser perceptível para o jogador | Média | Médio | Design explícito de feedback: o jogador DEVE perceber as consequências |

---

## Dependências

- [ ] `DESIGN_COMPASS.md` — Deve refletir esta visão.
- [ ] `docs/01_Game_Design_Document.md` — Deve detalhar a visão.
- [ ] `decisions/003_Design_Pillars.md` — Os pilares derivam desta visão.

---

## Consequências Futuras

**Portas abertas:**
- Sistema de facções com reputação.
- Economia dinâmica que reage ao jogador.
- Múltiplas resoluções para missões.
- Áreas secretas e conteúdo opcional.

**Portas fechadas:**
- Campanha linear roteirizada.
- Multiplayer competitivo.
- Conteúdo gerado proceduralmente (no escopo atual).

---

## Documentos Relacionados

- `DESIGN_COMPASS.md` — Documento de identidade do jogo.
- `PROJECT_CHARTER.md` — Documento de abertura do projeto.
- `AI_CONSTITUTION.md` — Regras constitucionais do projeto.

---

## Sistemas Afetados

- **Todos os sistemas** — Esta decisão define a direção de todo o projeto.

---

## Histórico de Alterações

| Versão | Data | Descrição | Autor |
|--------|------|-----------|-------|
| 1.0 | 2026-07-16 | Criação inicial | Diretor Criativo |
