# DEC-002 — Fantasia do Jogador

---

## Metadados

| Campo | Valor |
|-------|-------|
| **ID** | DEC-002 |
| **Título** | Fantasia do Jogador — Um Aventureiro em um Mundo Independente |
| **Data** | 2026-07-16 |
| **Autor** | Diretor Criativo / Lead Game Designer |
| **Status** | Aprovada |
| **Substitui** | — |
| **Substituída por** | — |

---

## Contexto

Com a visão do jogo definida (DEC-001), o próximo passo foi definir quem o jogador **se sente sendo** dentro do universo. A fantasia do jogador é a ponte entre a visão abstrata ("RPG sistêmico") e a experiência concreta ("o que eu sinto quando jogo").

Sem uma fantasia clara, decisões de design correm o risco de serem tecnicamente corretas mas emocionalmente vazias. Sistemas podem funcionar, mas não gerar a sensação desejada.

Foram considerados três arquétipos de fantasia:
- **O Herói Escolhido** (destino, salvação do mundo, narrativa épica).
- **O Sobrevivente** (escassez, perigo, superação).
- **O Aventureiro em um Mundo Vivo** (descoberta, agência, pertencimento conquistado).

---

## Problema

Qual sensação emocional queremos que o jogador experiencie durante toda a partida? Sem esta definição, mecânicas podem ser implementadas corretamente mas não evocar a emoção certa.

---

## Objetivo

Definir a fantasia do jogador de forma que:
- Direcione decisões de narrativa, arte e som.
- Informe o design de sistemas (como o jogador interage com o mundo).
- Crie consistência emocional em toda a experiência.

---

## Opções Consideradas

### Opção A: O Herói Escolhido

**Descrição:** O jogador é um personagem especial, destinado a salvar o mundo. A narrativa é o centro, e o mundo existe para servir à história do herói.

**Prós:**
- Fácil de comunicar e entender.
- Narrativa forte e direcionada.
- Apelo emocional imediato.

**Contras:**
- Conflita com mundo vivo (tudo gira em torno do jogador).
- Conflita com consequências (escolhas são ilusórias se o destino está traçado).
- Gera expectativa de campanha roteirizada, que não é o foco.

---

### Opção B: O Sobrevivente

**Descrição:** O jogador está em um ambiente hostil e precisa sobreviver. Escassez, perigo e superação são os temas centrais.

**Prós:**
- Engajamento por tensão constante.
- Sensação de progressão clara (sobreviver mais, prosperar).

**Contras:**
- Pode gerar ansiedade em vez de prazer exploratório.
- Incentiva comportamento conservador (não explorar por medo).
- Conflita com recompensa à curiosidade (pilar Exploração).

---

### Opção C: O Aventureiro em um Mundo Vivo (Escolhida)

**Descrição:** O jogador não é especial — é mais um habitante de Arkan. O que o torna único são suas ações. O mundo existe independentemente dele, e cabe a ele descobrir seu lugar, fazer escolhas e construir sua reputação. A fantasia é de **pertencimento conquistado**, não de **destino**.

**Prós:**
- Alinhamento total com os quatro pilares.
- Suporta histórias emergentes (cada jogador cria sua jornada).
- Mundo vivo faz sentido (não gira em torno do jogador).
- Consequências são naturais (ações definem reputação).
- Progressão de vulnerável a lendário é mais satisfatória.

**Contras:**
- Mais difícil de comunicar em materiais de marketing.
- Exige design cuidadoso para que o jogador perceba o impacto de suas ações.
- Jogadores acostumados com narrativa guiada podem se sentir perdidos.

---

## Alternativa Escolhida

**Decisão:** Opção C — O Aventureiro em um Mundo Vivo.

---

## Justificativa Técnica

A Opção C é a única que suporta todos os quatro pilares de design simultaneamente:

| Pilar | Como a Opção C o suporta |
|-------|-------------------------|
| **Exploração** | O jogador explora porque quer descobrir, não porque a história mandou. A descoberta é a recompensa. |
| **Mundo Vivo** | O mundo não gira em torno do jogador. Faz sentido que NPCs tenham vidas, que a economia flua, que estações mudem. |
| **Consequências** | Se o jogador não é especial, suas ações são o que o define. Escolhas têm peso real. |
| **Progressão** | A jornada de "ninguém" a "lenda" é mais longa e mais satisfatória. Cada conquista é mérito do jogador. |

Além disso, esta fantasia **reduz a necessidade de conteúdo roteirizado** (diálogos, cutscenes, animações), permitindo que o desenvolvedor solo foque em sistemas.

---

## Impactos Positivos

- Consistência entre visão, pilares e experiência do jogador.
- Suporte natural a histórias emergentes.
- Menos dependência de conteúdo roteirizado.
- Reforça a identidade única do jogo.

---

## Impactos Negativos

- Exige que o jogador seja proativo (pode não agradar quem prefere jogos guiados).
- Comunicação da proposta é mais desafiadora.
- Risco de jogadores não perceberem o mundo vivo se o feedback não for explícito.

---

## Riscos

| Risco | Probabilidade | Impacto | Mitigação |
|-------|:------------:|:-------:|-----------|
| Jogador não percebe que o mundo é "vivo" | Alta | Alto | Feedback explícito: mudanças visíveis no mapa, NPCs comentarem ações, economia mostrar flutuações |
| Jogador se sente perdido sem direção | Média | Médio | Missão principal leve como guia, mas sem forçar caminho. Sistema de dicas não intrusivo. |
| Fantasia difícil de comunicar em marketing | Alta | Médio | Trailer focado em mostrar o mundo reagindo, não em narrativa épica |

---

## Dependências

- [ ] `DESIGN_COMPASS.md` — Já reflete esta fantasia (seção 4).
- [ ] `docs/05_Lore.md` — Lore deve suportar esta fantasia (mundo existe antes do jogador).
- [ ] `docs/07_NPCs.md` — NPCs com rotinas independentes.
- [ ] `docs/15_Economia.md` — Economia que funciona sem o jogador.

---

## Consequências Futuras

**Portas abertas:**
- Sistema de reputação (ações definem relacionamento com facções).
- Missões com múltiplas resoluções baseadas em escolhas.
- Mundo que muda visivelmente com o tempo (cidades crescem, áreas se degradam).

**Portas fechadas:**
- Narrativa onde o jogador é o "escolhido" ou "salvador".
- Cutscenes longas e roteirizadas.
- Missões principais obrigatórias lineares (missões existem, mas podem ser ignoradas).

---

## Documentos Relacionados

- `DESIGN_COMPASS.md` (seção 4 — Fantasia do Jogador).
- `DEC-001` — Visão do Jogo (decisão da qual esta deriva).
- `DEC-003` — Pilares de Design (pilares que esta fantasia suporta).
- `docs/05_Lore.md` — Lore do mundo.

---

## Sistemas Afetados

- **Narrativa / Lore** — Deve refletir mundo independente.
- **NPCs** — Rotinas e reatividade às ações do jogador.
- **Missões** — Estrutura não linear.
- **Economia** — Flutuação independente.
- **Reputação** — Sistema derivado desta fantasia.

---

## Histórico de Alterações

| Versão | Data | Descrição | Autor |
|--------|------|-----------|-------|
| 1.0 | 2026-07-16 | Criação inicial | Diretor Criativo |
