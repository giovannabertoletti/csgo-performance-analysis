# Análise de Performance em Esports (CS:GO)

## 📍 Contexto
Este projeto tem como objetivo analisar a performance de jogadores e equipes de CS:GO ao longo do tempo,  
indo além de métricas médias e considerando consistência, impacto, perfil de jogo e contexto competitivo.

No cenário profissional de CS:GO, performance não pode ser avaliada apenas por números isolados como K/D ou Win Rate.  
O desempenho real é fortemente influenciado por fatores como **função exercida no time**, **estilo de jogo**, **uso de utilitários**, **impacto inicial nos rounds** e **capacidade de manter desempenho em momentos críticos**.

Como o dataset utilizado é **agregado por jogador**, a análise não observa decisões round a round.  
Em vez disso, o projeto busca identificar **padrões de impacto, consistência e propensão à tomada de decisão em momentos críticos**, inferidos a partir de métricas consolidadas como opening kills, conversão de vantagem inicial e ocorrência de multi-kill rounds.

A motivação deste projeto surge da necessidade de interpretar performance como algo **dinâmico e multifatorial**,  
onde estatísticas isoladas não explicam completamente o impacto real de um jogador dentro do jogo.

---

## 🎯 Problema
Métricas médias como K/D ou Win Rate, quando analisadas isoladamente, podem esconder:

- instabilidade de desempenho ao longo do tempo  
- picos ocasionais que não se sustentam  
- diferenças relevantes entre jogadores com médias semelhantes  
- mau aproveitamento de função e estilo de jogo  
- impacto reduzido em momentos decisivos  

O desafio foi identificar **padrões de performance mais realistas**, considerando não apenas volume de dados, mas principalmente **qualidade de impacto e consistência ao longo de muitos rounds jogados**.

---

## 📊 Dados
- **Fonte:** Dataset público de CS:GO (nível jogador agregado)  
- **Tipo:** Estatísticas consolidadas por jogador  
- **Principais colunas:**
  - jogador  
  - mapas e rounds jogados  
  - kills, deaths, K/D  
  - ADR (damage per round)  
  - rating  
  - opening kills, opening deaths e opening kill ratio  
  - team win % after first kill  
  - sniper kills, rifle kills, grenade kills  
  - rounds com 3, 4 e 5 kills  

---

## 🔍 Dimensões de Análise de Performance

### 🎯 Performance Individual
Avalia impacto e eficiência do jogador ao longo de grande volume de rounds.

- **K/D e ADR**  
- **Rating**  
- **Impacto médio por round**  
- **Consistência ao longo do tempo**  
- **Volume de rounds jogados (amostra)**  

Essas métricas ajudam a diferenciar jogadores explosivos de jogadores consistentes.

---

### 🧠 Perfil de Jogo e Função
A partir dos dados disponíveis, é possível inferir **perfil e função natural** do jogador.

- Perfil AWP (sniper kills elevados)  
- Perfil rifle / entry  
- Perfil equilibrado  
- Jogadores de impacto inicial (opening kills)  
- Jogadores de fechamento de round (multi-kill rounds)  

Essa leitura auxilia na **alocação mais eficiente de funções**, evitando análises injustas baseadas apenas em média geral.

---

### ⚡ Reação Inicial e Impacto Tático
A capacidade de reagir rapidamente e gerar vantagem inicial é inferida por:

- **Opening kill ratio**  
- **Total de opening kills**  
- **Conversão da first kill em vitória de round**  

Essas métricas funcionam como proxy de **leitura inicial, reação rápida e impacto tático**, fundamentais para o ritmo do jogo.

---

### 🔥 Decisão em Momentos Críticos (Proxy)
Como o dataset não é round-level, a tomada de decisão sob pressão é analisada de forma indireta.

A propensão à decisão em momentos críticos é inferida por:
- frequência de **multi-kill rounds (3K, 4K, 5K)**  
- manutenção de **rating elevado em alto volume de rounds**  
- impacto consistente em cenários de alta exigência  

Essa abordagem permite identificar jogadores que mantêm clareza e impacto mesmo quando o round exige execução precisa, sem assumir leitura direta de processos cognitivos.

---

### 🧭 Liderança e Influência Tática (Inferência)
O projeto também permite inferir **potencial de liderança tática**, a partir de jogadores que combinam:

- alto impacto individual  
- boa taxa de opening kills  
- elevada conversão de vantagem inicial  
- consistência ao longo do tempo  

Esses padrões não definem formalmente o papel de IGL, mas indicam jogadores com **perfil de influência estratégica e tomada de decisão**.

---

## 📈 Dashboard
O dashboard foi desenvolvido no **LookerStudio**, com foco em:

- impacto vs consistência dos jogadores  
- reação inicial e conversão de vantagem  
- propensão à decisão em momentos críticos  
- identificação de perfis de jogo e possíveis lideranças  

👉 **Link para o LookerStudio:**  
cxxxxxxxx

---

## 💡 Principais Insights
- Jogadores com médias semelhantes podem apresentar perfis de impacto completamente diferentes.  
- Consistência é tão importante quanto pico de performance.  
- Opening kills e multi-kill rounds são fortes indicadores de impacto decisivo.  
- Nem todo jogador de alto K/D é o mais influente nos momentos críticos.  

---

## 🧭 Aplicação Prática
Essa análise pode apoiar decisões relacionadas a:

- definição e ajuste de funções dentro do time  
- identificação de jogadores mais consistentes ou mais explosivos  
- leitura de impacto em momentos decisivos  
- planejamento estratégico e scouting de jogadores  

---

📌 Para acompanhar a evolução do projeto, consulte o [ROADMAP](ROADMAP.md).
