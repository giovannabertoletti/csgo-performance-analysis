
# Análise de Performance em Esports (CS:GO)

## 📍 Contexto
Este projeto tem como objetivo analisar a performance de jogadores e equipes de CS:GO ao longo do tempo,  
indo além de métricas médias e considerando consistência, picos, quedas, contexto de jogo e as possíveis consequências que cada resultado pode gerar.

No contexto competitivo de CS:GO, performance não pode ser avaliada apenas por números isolados como K/D ou Win Rate.  
O desempenho real é fortemente influenciado por fatores como **função exercida no time**, **uso de utilitários**, **mapa jogado**, **lado (TR/CT)**, **economia do round**, **timing das decisões** e **situações de pressão**.

A motivação deste projeto surge da necessidade de interpretar performance como algo **dinâmico e multifatorial**,  
onde estatísticas isoladas não explicam completamente o impacto real de um jogador ou time dentro do jogo.

---

## 🎯 Problema
Métricas médias como K/D ou Win Rate, quando analisadas isoladamente, podem esconder:

- instabilidade de desempenho ao longo do tempo  
- picos ocasionais que não se sustentam  
- diferenças relevantes entre jogadores com médias semelhantes  
- desconforto posicional e mau aproveitamento de função  
- baixa consistência em situações de pressão  

O desafio foi identificar **padrões de performance mais realistas**, considerando não apenas o volume de dados, mas principalmente o **contexto em que eles ocorrem**.

---

## 📊 Dados
- **Fonte:** Dataset público de CS:GO  
- **Tipo:** Estatísticas de partidas  
- **Principais colunas:**
  - jogador  
  - data da partida  
  - mapa  
  - lado (TR / CT)  
  - kills, deaths, ADR  
  - first kills, first bloods  
  - uso de AWP  
  - utilitários (flashbang, smoke, molotov, HE)  
  - estilo de jogo / função  
  - resultado da partida (win/loss)  
  - plant da C4 e cover para plant  
  - armas utilizadas  
  - jogadas e situações de round  

---

## 🔍 Dimensões de Análise de Performance

### 🎯 Performance Individual
Avalia o impacto direto e a consistência do jogador ao longo das partidas.

- **K/D e ADR**  
- **Impacto por round**  
- **Consistência** (jogos bons vs jogos ruins)  
- **Performance por lado** (TR / CT)  
- **Performance segmentada por mapa**  
- **Performance segmentada por função**

Essas métricas ajudam a identificar **onde cada jogador rende melhor**, evitando análises distorcidas baseadas apenas em média geral.

---

### 🧠 Funções e Papéis no Time
Cada função apresenta riscos, responsabilidades e padrões de impacto diferentes, exigindo métricas específicas.

- **Entry fragger:** taxa de sucesso em entradas e geração de espaço  
- **Trader / Second entry:** efetividade de troca e resposta rápida  
- **AWPer:** first kill, first death e controle de ângulos  
- **Suporte:** uso e efetividade de utilitários  
- **Lurker:** impacto indireto, tempo ganho e leitura de mapa  
- **IGL:** impacto em decisões, mid-round calls e adaptação  

Essa leitura permite melhor aproveitamento dos jogadores e ajustes mais inteligentes de função e posição.

---

### 💣 Uso de Utilitários
Utilidade bem aplicada frequentemente decide rounds, mesmo sem kills diretas.

- Smokes efetivas  
- Flash assists  
- Dano causado por HE  
- Molotovs que forçam movimentação  
- Utilidade desperdiçada  

A análise de utilitários evidencia **inteligência tática** e impacto invisível no resultado das partidas.

---

### 🗺️ Map Pool e Controle de Espaço
A performance varia significativamente de acordo com o mapa e o lado jogado.

- Win rate por mapa  
- Lado mais forte e mais fraco (TR / CT)  
- Bombsites mais perdidos  
- Execuções mais eficientes  
- Mapas prioritários para veto  

Esses dados auxiliam na preparação de campeonatos, leitura de conforto do time e decisões estratégicas de veto.

---

### 🔁 Padrões Coletivos do Time
Identifica comportamentos recorrentes que podem ser explorados ou ajustados.

- Rounds ganhos após perder pistol  
- Efetividade em eco e force buy  
- Tendências previsíveis de jogo  
- Velocidade de rotação  
- Reação coletiva após perder um jogador  

Quebrar padrões previsíveis reduz a leitura do adversário e melhora a adaptabilidade do time.

---

### ⏱️ Timing, Reação e Tomada de Decisão
Avalia a qualidade das decisões sob restrição de tempo e informação.

- Tempo médio de execução  
- Mortes por pressa vs atraso  
- Sucesso de rush vs split  
- Rounds decididos no mid  
- Resposta imediata após eventos críticos  

Essa análise melhora calls, leitura de jogo e adaptação em tempo real.

---

### 🧠 Raciocínio Lógico e Decisão Sob Pressão
Além da velocidade de reação, o projeto considera a capacidade de **raciocínio lógico sob pressão**, essencial em rounds competitivos.

O raciocínio lógico está associado à habilidade de:
- avaliar riscos com informação limitada  
- antecipar comportamentos adversários  
- adaptar decisões em tempo real  
- reduzir erros evitáveis em momentos críticos  

A análise busca identificar padrões indiretos de decisão a partir de:
- comportamento em desvantagem numérica  
- adaptação em mid-round  
- consistência decisional ao longo das partidas  

Jogadores com bom raciocínio lógico tendem a **perder melhor quando perdem**, mantendo impacto estratégico e reduzindo danos ao coletivo.

---

### ⚡ Decisão Sob Pressão, Liderança e Comportamento
Este projeto também analisa **padrões de decisão sob pressão** para entender liderança, perfil comportamental e tomada de decisão coletiva.

Situações analisadas incluem:
- clutches e retakes  
- rounds decisivos  
- resposta após perder um teammate  
- sequências negativas  

A partir desses cenários, são avaliados indicadores indiretos como:
- taxa de trades em situações críticas  
- mortes não justificadas sob pressão (considerando função e contexto)  
- uso de utilidade em momentos decisivos  
- sucesso em clutches e retakes  

Esses indicadores são visualizados em um **gráfico de dispersão**, comparando:
- **qualidade da decisão sob pressão**
- **performance em cenários críticos**

Com destaque para o **capitão (IGL)**, essa abordagem permite identificar:
- líderes naturais dentro do time  
- jogadores que mantêm clareza sob pressão  
- perfis comportamentais complementares  
- oportunidades de ajuste de função e comunicação  

---

## 📈 Dashboard
O dashboard foi desenvolvido no **Tableau**, com foco em:

- evolução temporal da performance  
- identificação de picos e quedas  
- comparação entre média e consistência  
- leitura contextual dos resultados  
- visualização de decisão sob pressão e liderança  

👉 **Tableau Public:** vo coloca aqui o link

---

## 💡 Principais Insights
- Jogadores com médias semelhantes podem apresentar níveis de consistência completamente diferentes.  
- A média isolada não representa adequadamente a performance real.  
- Utilidade bem aplicada pode impactar mais rounds do que kills diretas.  
- Decisão sob pressão diferencia jogadores e líderes dentro do time.  
- Boa alocação de função reduz erros e potencializa performance coletiva.  

---

## 🧭 Aplicação Prática
Essa análise pode apoiar decisões relacionadas a:

- ajustes de treino individual e coletivo  
- definição e redistribuição de funções  
- gestão emocional e tomada de decisão sob pressão  
- leitura de liderança e comunicação  
- preparação de campeonatos e vetos de mapa  

---


