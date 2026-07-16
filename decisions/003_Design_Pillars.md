# DEC-003 — Pilares de Design

---

## Metadados

| Campo | Valor |
|-------|-------|
| **ID** | DEC-003 |
| **Título** | Pilares de Design — Exploração, Mundo Vivo, Consequências e Progressão |
| **Data** | 2026-07-16 |
| **Autor** | Diretor Criativo / Lead Game Designer |
| **Status** | Aprovada |
| **Substitui** | — |
| **Substituída por** | — |

---

## Contexto

Com a visão do jogo (DEC-001) e a fantasia do jogador (DEC-002) definidas, o próximo passo foi estabelecer os **pilares de design** — os quatro fundamentos sobre os quais todas as mecânicas, sistemas e conteúdos serão construídos.

Os pilares funcionam como os "ossos" do projeto. Eles não mudam. Toda funcionalidade, sistema ou conteúdo deve servir a pelo menos um pilar — idealmente mais de um.

Foram propostos seis pilares iniciais. Após análise, quatro foram escolhidos e dois foram descartados ou absorvidos.

---

## Problema

Sem pilares definidos, não há critério objetivo para avaliar se uma funcionalidade pertence ao jogo. Decisões de design tornam-se subjetivas ("eu acho legal") em vez de baseadas em princípios.

---

## Objetivo

Estabelecer 3 a 5 pilares de design que:
- Sejam distintos entre si (sem sobreposição).
- Sejam acionáveis (cada pilar gera diretrizes concretas).
- Cubram toda a experiência do jogo.
- Possam ser usados para avaliar qualquer proposta de funcionalidade.

---

## Opções Consideradas

### Pilares Propostos Inicialmente

1. **Exploração** — Descobrir o mundo é a atividade central.
2. **Mundo Vivo** — O mundo funciona independentemente do jogador.
3. **Consequências** — Escolhas geram resultados perceptíveis.
4. **Progressão** — Evolução tangível e transformadora.
5. **Combate** — Conflito como ferramenta de engajamento.
6. **Crafting** — Criação como expressão do jogador.

### Análise de Sobreposição

| Par de Pilares | Sobreposição | Decisão |
|----------------|:-----------:|---------|
| Combate + Progressão | Alta — Combate é uma ferramenta de progressão | Combate absorvido por Progressão |
| Crafting + Progressão | Alta — Crafting é uma ferramenta de progressão | Crafting absorvido por Progressão |
| Crafting + Consequências | Média — Crafting pode gerar consequências econômicas | Mantido como sub-sistema |

### Resultado

Após análise, Combate e Crafting foram removidos como pilares independentes porque:
- **Combate** é um **meio**, não um fim. Ele serve à Exploração (derrotar guardiões de áreas) e à Progressão (novas armas = novas possibilidades). Não precisa de pilar próprio.
- **Crafting** é uma **ferramenta de progressão**. O que importa não é craftar, mas o que craftar permite fazer. Crafting sem progressão vira simulador.

---

## Alternativa Escolhida

**Decisão:** Quatro pilares — Exploração, Mundo Vivo, Consequências, Progressão.

---

## Justificativa Técnica

### Pilar 1 — Exploração

**Definição:** O ato de descobrir o mundo é a atividade central do jogo.

**Por que é um pilar:** Sem exploração, o jogo perde sua identidade. É o que diferencia Legends of Arkan de um simulador de crafting ou de um jogo de combate genérico.

**Diretrizes de design:**
- Mapas não lineares com múltiplas entradas e saídas.
- Segredos visíveis mas de acesso não óbvio.
- Recompensas fora do caminho principal (desvio sempre vale a pena).
- Minimapa que mostra terreno mas não revela pontos de interesse.
- Nenhuma habilidade crítica no caminho principal (o jogador precisa explorar para evoluir).

**Exemplo prático:** Uma ponte quebrada não é um obstáculo — é um convite. O jogador vê que há algo do outro lado, anota mentalmente, e volta quando tiver as ferramentas certas.

**O que evitar:** Corredores lineares, waypoints automáticos, checklists de "100% do mapa".

---

### Pilar 2 — Mundo Vivo

**Definição:** O mundo funciona independentemente do jogador. NPCs têm rotinas, a economia flutua, criaturas se comportam conforme seu habitat.

**Por que é um pilar:** Um mundo que só existe quando o jogador está presente quebra a imersão. O jogador precisa sentir que Arkan existia antes dele e continuará existindo depois.

**Diretrizes de design:**
- NPCs com rotinas diárias (acordar, trabalhar, socializar, dormir).
- Ciclo dia/noite com impacto em gameplay (lojas fecham, criaturas noturnas aparecem).
- Estações climáticas que afetam recursos e comportamento.
- Economia com oferta e demanda (preços variam com ações do jogador e tempo).
- Inimigos não spawnam magicamente — têm territórios, migram, e podem ser extintos.

**Exemplo prático:** O ferreiro fecha a loja às 18h e vai para taverna. Se o jogador chegar atrasado, pode arrombar a loja (consequência: reputação negativa com a guilda dos ferreiros) ou esperar até o próximo dia.

**O que evitar:** NPCs estáticos no mesmo lugar 24h, lojas com estoque infinito, tempo congelado até o jogador interagir.

---

### Pilar 3 — Consequências

**Definição:** Escolhas relevantes geram consequências perceptíveis e duradouras.

**Por que é um pilar:** Se as escolhas não importam, o jogo é uma ilusão. Consequências são o que tornam a progressão significativa e o mundo vivo crível.

**Diretrizes de design:**
- Missões com pelo menos 2 resoluções possíveis.
- Sistema de reputação por facção (ações abrem e fecham portas).
- Economia que reage a ações do jogador (matar todos os lobos → pele mais barata).
- Mudanças permanentes no mapa (cidades que crescem, áreas que se degradam).
- Consequências não são binárias (bom vs mau) — são relacionais (facção A vs facção B).

**Exemplo prático:** Ajudar a guilda dos mineradores dá acesso a minérios raros, mas fecha a guilda dos ferreiros artesãos. O jogador não pode maximizar reputação com ambos — precisa escolher.

**O que evitar:** Escolhas falsas (mesmo resultado), consequências puramente cosméticas, sistema de moralidade binário, possibilidade de "farmar" reputação com todos.

---

### Pilar 4 — Progressão

**Definição:** O jogador evolui de forma tangível e transformadora. Cada novo item, habilidade ou conhecimento muda a forma como o jogo é jogado.

**Por que é um pilar:** Progressão puramente numérica (+5 de dano) não sustenta engajamento de longo prazo. O jogador precisa sentir que **joga diferente** após cada upgrade significativo.

**Diretrizes de design:**
- Itens que desbloqueiam novas formas de interagir com o mundo (picareta → mineração, bota de gelo → travessia de água congelada).
- Habilidades que alteram gameplay (não apenas aumentam números).
- Crafting com trade-offs (velocidade vs dano, defesa vs mobilidade).
- Árvore de habilidades que permite especialização (não é possível ter tudo).
- Progressão de "vulnerável" a "lenda" com marcos visíveis.

**Exemplo prático:** Um cajado de gelo não é "dano mágico +15". Ele permite congelar superfícies de água, criando plataformas para alcançar áreas antes inacessíveis. Isso é progressão — não um número, mas uma **nova possibilidade**.

**O que evitar:** Upgrades que são apenas números maiores, habilidades que não mudam gameplay, árvore de habilidades que permite pegar tudo.

---

## Impactos Positivos

- Critérios objetivos para avaliar funcionalidades (Teste da Bússola).
- Direção clara para todos os sistemas do jogo.
- Facilita a identificação de funcionalidades fora de escopo.
- Documentação de design mais enxuta (cada sistema sabe a que pilar serve).

---

## Impactos Negativos

- Reduz flexibilidade criativa (funcionalidades que não servem a nenhum pilar são descartadas).
- Exige disciplina para não adicionar "só porque é legal".
- Alguns jogadores podem sentir falta de elementos descartados (combate mais profundo, crafting mais complexo).

---

## Riscos

| Risco | Probabilidade | Impacto | Mitigação |
|-------|:------------:|:-------:|-----------|
| Pilares muito abstratos para guiar decisões do dia a dia | Média | Alto | Exemplos práticos detalhados neste documento. Teste da Bússola com perguntas concretas. |
| Funcionalidade que serve a 2+ pilares mas é ruim em todos | Baixa | Médio | Teste da Bússola exige mínimo de 5/8 pontos. Abaixo disso, a funcionalidade é rejeitada. |
| Pressão para adicionar pilar extra (ex: "Combate precisa de pilar próprio") | Média | Baixo | Combate e Crafting são ferramentas, não pilares. Justificativa documentada. |

---

## Dependências

- [ ] `DESIGN_COMPASS.md` (seção 5) — Deve refletir estes pilares exatamente.
- [ ] `docs/01_Game_Design_Document.md` — Deve detalhar cada pilar em termos de gameplay.
- [ ] `docs/06_Mecanicas.md` — Cada mecânica deve referenciar o pilar que serve.
- [ ] `decisions/001_Game_Vision.md` — Visão da qual estes pilares derivam.
- [ ] `decisions/002_Player_Fantasy.md` — Fantasia que estes pilares suportam.

---

## Consequências Futuras

**Portas abertas:**
- Sistema de reputação (suporta Consequências e Mundo Vivo).
- Ferramentas com usos múltiplos (suporta Progressão e Exploração).
- Economia dinâmica (suporta Mundo Vivo e Consequências).
- Ciclo dia/noite e estações (suporta Mundo Vivo).

**Portas fechadas:**
- Combate como foco central (é meio, não pilar).
- Sistema de crafting complexo independente (é ferramenta de progressão).
- Habilidades puramente passivas (não transformam gameplay).
- Progressão linear obrigatória (conflita com Exploração).

---

## Documentos Relacionados

- `DESIGN_COMPASS.md` (seção 5 — Os Quatro Pilares do Design).
- `DEC-001` — Visão do Jogo.
- `DEC-002` — Fantasia do Jogador.
- `docs/06_Mecanicas.md` — Detalhamento das mecânicas.
- `docs/12_Sistema_Combate.md` — Combate como ferramenta de progressão.
- `docs/14_Sistema_Crafting.md` — Crafting como ferramenta de progressão.

---

## Sistemas Afetados

- **Todos os sistemas** devem ser avaliados contra estes pilares.
- **Sistema de Combate** — Deve servir à Exploração e Progressão, não ser um fim em si.
- **Sistema de Crafting** — Deve servir à Progressão, com trade-offs significativos.
- **Sistema de Missões** — Deve suportar Consequências (múltiplas resoluções).
- **Sistema de Economia** — Deve suportar Mundo Vivo (flutuação independente).
- **Sistema de NPCs** — Deve suportar Mundo Vivo (rotinas) e Consequências (reputação).
- **Sistema de IA** — Deve suportar Mundo Vivo (comportamento independente).

---

## Histórico de Alterações

| Versão | Data | Descrição | Autor |
|--------|------|-----------|-------|
| 1.0 | 2026-07-16 | Criação inicial | Diretor Criativo |
