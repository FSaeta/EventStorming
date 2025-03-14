# 📌 Roteiro para a Atividade de Event Storming

## **1️⃣ Preparação (5-10 min)**
  Agendamento de Partidas
---

## **2️⃣ Mapeamento de Eventos de Domínio (15-20 min)**
- Pergunta-chave: **"O que acontece no processo?"** *(sempre no passado)*
- Cada grupo lista eventos importantes.
  - **Partida Criada (Quando um evento esportivo é agendado)**
  - **Local Reservado (Quando um local é confirmado)**
  - **Time Formado (Quando uma equipe é formada para a partida)**
  - **Jogadores Confirmados (Quando todos os jogadores são confirmados para a partida)**
  - **Partida Iniciada (Quando a partida começa)**
  - **Partida Concluída (Quando a partida é finalizada)**
  - **Organizar os eventos em ordem cronológica.**

---

## **3️⃣ Identificação de Comandos e Atores (10-15 min)**
- Pergunta-chave: **"O que causou esse evento?"**
- Relacionar **comandos** (ações ativas) com os **atores** (usuários ou sistemas externos).
- **Comando: Criar Partida**

- **Ator: Administrador**
  - **Evento gerado: Partida Criada**
  - **Comando: Formar Time**

- **Ator: Jogador ou Sistema (Gerenciamento de Times)**
  - **Evento gerado: Time Formado**
  - **Comando: Confirmar Local**

- **Ator: Sistema ou Administrador**
  - **Evento gerado: Local Reservado**
  - **Comando: Confirmar Participação**

- **Ator: Jogador**
  - **Evento gerado: Jogadores Confirmados**
  - **Comando: Iniciar Partida**

- **Ator: Árbitro**
  - **Evento gerado: Partida Iniciada**

---

## **4️⃣ Descobrindo Regras e Políticas de Negócio (10-15 min)**
- Pergunta-chave: **"Quais regras precisam ser seguidas nesse processo?"**
- Identificar **políticas** (regras automáticas ou manuais).
- **Regra 1: Se um jogador não tem o nível técnico compatível, ele não pode ser adicionado ao time.**
- **Regra 2: O local da partida só pode ser confirmado se houver a disponibilidade para o horário solicitado.**
- **Regra 3: A partida só pode ser iniciada se todos os jogadores estiverem confirmados.**

---

## **5️⃣ Identificação dos Bounded Contexts (10 min)**
- Pergunta-chave: **"Quem é responsável por cada parte do processo?"**
- Separar os eventos e comandos em **diferentes áreas do sistema**.

- **Bounded Context: Agendamento de Partidas**
  - **Comandos: Criar Partida, Confirmar Local**
  - **Eventos: Partida Criada, Local Reservado**
  - **Responsável: Sistema de Agendamento**

- **Bounded Context: Gerenciamento de Times**
  - **Comandos: Formar Time**
  - **Eventos: Time Formado**
  - **Responsável: Gerenciamento de Times**

- **Bounded Context: Players**
  - **Comandos: Confirmar Participação**
  - **Eventos: Jogadores Confirmados**
  - **Responsável: Players**

- **Bounded Context: Esportes**
  - **Comandos: Validar Regras do Esporte**
  - **Eventos: Regras Validadas**
  - **Responsável: Sistema de Esportes**

---

## **6️⃣ Discussão e Refinamento (15 min)**
- Cada grupo apresenta seu fluxo.
  

---
