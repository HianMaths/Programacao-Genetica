# 🧠 Programação Genética Aplicada ao Controle de Robôs

Este repositório contém a implementação e aprimoramentos de um sistema de **Programação Genética (PG)** voltado para o controle de um robô autônomo em um ambiente 2D com obstáculos, recursos e uma meta final.

## 📌 Objetivo

Evoluir o comportamento de um robô para navegar de forma eficiente, evitando obstáculos, coletando recursos e atingindo uma meta, com base em árvores de decisão geradas via Programação Genética.

---

## ⚙️ Estrutura do Projeto

O projeto se baseia nos seguintes arquivos:

* `robo_exercicio.py`: Versão aprimorada desenvolvida pelo grupo.
* `Evolução_fitness`: Imagem mostrando a evolução do robo.
* `Programao_Genetica...`: pdf explicativo com o que foi pedido para ser feito.

---

## ✅ Melhorias Implementadas

### 🔧 Algoritmo Genético (`IndividuoPG` e `ProgramacaoGenetica`)

* **Novos Operadores Funcionais**:

  * Adicionados: `sin`, `cos`, `tanh`, `sqrt`, `log`, `pow`
  * Esses operadores ampliam a diversidade de expressões evoluídas e permitem comportamentos mais sofisticados.

* **Fitness Refinado**:

  * Rebalanceado para enfatizar **meta atingida**, penalizar **colisões** e **energia gasta**.
  * Novo bônus adicional caso todos os recursos sejam coletados.
  * Incentivo substancial ao atingir a meta final: `+5000` pontos (aumentado).

* **Parâmetros de Evolução Ajustados**:

  * População: `500` indivíduos (aumentado).
  * Profundidade das árvores: `5` (aumentado).
  * Gerações: `50`.
  * Elitismo: `10%` dos melhores preservados (mais forte).
  * Tentativas por indivíduo: `3` (reduzido para acelerar o processo).
  * Taxa de mutação adaptativa baseada no fitness relativo do indivíduo.

* **Seleção Aprimorada**:

  * Seleção por torneio com tamanho adaptativo proporcional ao fitness médio da população, promovendo pressão seletiva variável.

* **Diversidade Genética**:

  * A mutação agora permite mais variação e combinações de operadores, ajudando a evitar convergência prematura.

### 🤖 Simulação (`Ambiente`, `Robo`, `Simulador`)

As classes de simulação foram mantidas conforme recomendado, com pequenas **adições pontuais para suporte às novas regras de avaliação**, como:

* Reforço na visualização da meta.
* Acompanhamento do status de **meta atingida** em tempo real.
* Melhor organização visual da simulação (textos e grades).

---

## 👥 Participantes

Este projeto foi desenvolvido em grupo, com contribuição colaborativa de todos os membros.
