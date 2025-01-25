# Cyclistic Insights

## Sobre
A Cyclistic é uma empresa de compartilhamento de bicicletas lançada em 2016 que opera uma rede com mais de 5.800 bicicletas e 692 estações em Chicago. A equipe financeira identificou que membros anuais são mais lucrativos do que ciclistas casuais. Com isso, a diretora de marketing Lily Moreno propôs o objetivo de converter ciclistas casuais em membros anuais, aproveitando insights dos dados de uso e campanhas digitais estratégicas.

---

## Cenário
A análise revelou três principais conclusões:
- **Diferentes Padrões de Uso**: Membros anuais utilizam bicicletas para transporte diário, enquanto os casuais usam para lazer nos finais de semana.
- **Motivação para Adesão**: Ciclistas casuais buscam economia e conveniência oferecidas por planos anuais.
- **Marketing Digital**: Campanhas que destacam economia, flexibilidade e histórias reais de usuários são mais eficazes para aumentar a adesão.

---

## Ask
O objetivo é analisar dados históricos de viagens para entender como os membros anuais e os ciclistas casuais utilizam as bicicletas de forma diferente. Esses insights ajudarão na criação de estratégias de marketing direcionadas para converter ciclistas casuais em membros anuais.

**Stakeholders:**
- Lily Moreno: Diretora de Marketing
- Equipe de Análise de Marketing da Cyclistic
- Equipe Executiva da Cyclistic

---

## Prepare
Foi utilizado o conjunto de dados público da Cyclistic, fornecido pela [Motivate International Inc.](https://divvy-tripdata.s3.amazonaws.com/index.html).  
Os dados passaram por verificações de inconsistências, análise de valores ausentes e validação geral.

---

## Process
### Etapas no Excel
#### **1. Criação da Coluna `ride_length`**
- Fórmula: `=D2-C2` (onde D2 é o horário de término e C2 é o horário de início).
- Resultado: Nova coluna indicando a duração da viagem.

#### **2. Criação da Coluna `day_of_week`**
- Fórmula: `=DIA.DA.SEMANA(C2,1)`  
  - Retorna o dia da semana da viagem (domingo = 1, sábado = 7).

---

## Analyze
### Cálculos Realizados:
1. **Média de `ride_length`:**
   - Fórmula: `=MÉDIA(N:N)`  
   - Resultado: A duração média de todas as viagens.

2. **Máximo de `ride_length`:**
   - Fórmula: `=MÁXIMO(N:N)`  
   - Resultado: A viagem mais longa registrada.

3. **Moda de `day_of_week`:**
   - Fórmula: `=MODA(N:N)`  
   - Resultado: O dia mais comum para as viagens.

### Tabelas Dinâmicas:
1. **Média de `ride_length` para Membros e Casuais**
   - Linhas: `member_casual`  
   - Valores: Média de `ride_length`  
   - Resultado: Identificação de diferenças na duração média entre os grupos.

2. **Média de `ride_length` por Dia da Semana**
   - Colunas: `day_of_week`  
   - Linhas: `member_casual`  
   - Valores: Média de `ride_length`  
   - Resultado: Tendências ao longo da semana para membros e casuais.

3. **Contagem de Viagens por Dia da Semana**
   - Colunas: `day_of_week`  
   - Linhas: `member_casual`  
   - Valores: Contagem de `ride_id`  
   - Resultado: Volume de viagens por dia e tipo de usuário.

---

## Share
### Visualizações Criadas:
1. **Média de `ride_length` para Membros e Casuais**  
   ![Média de ride_length para Membros e Casuais](https://github.com/user-attachments/assets/315728e3-b3ef-4b7f-8802-3fee30fbcb2e)

2. **Média de `ride_length` por Dia da Semana**  
   ![Média de ride_length por Dia da Semana](https://github.com/user-attachments/assets/e0354d5f-0db1-4633-8588-4ed27397cccb)

3. **Contagem de Viagens por Dia da Semana**  
   ![Contagem de Viagens por Dia da Semana](https://github.com/user-attachments/assets/acca6750-a210-47f5-808c-8f4b67d2cc86)

---

## Conclusão
- Membros anuais utilizam as bicicletas de forma mais regular e durante a semana, enquanto usuários casuais têm maior volume de viagens aos finais de semana.
- Estratégias de marketing devem focar nos casuais, destacando a conveniência e economia do plano anual.

### Próximos Passos:
1. Refinar as visualizações para apresentações executivas.
2. Desenvolver campanhas digitais específicas baseadas nos padrões identificados.
