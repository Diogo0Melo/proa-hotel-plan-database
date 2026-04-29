<h1 align="center"><a href="./TasokareHotel/Instructions/README.md" target="_blank">🏨 Hotel Tasokare - Planejamento</a></h1>

<img width="2752" height="1536" alt="A_wide_16_9_202604221302" src="https://github.com/user-attachments/assets/27ad1b2f-b5d0-454e-a9ac-2feb4d2fca7c" />
<br>

Projeto de estruturação e modelagem de um banco de dados não relacional (NoSQL) para a gestão completa da rede hoteleira Hotel Tasokare.

---

## 📁 Estrutura do Projeto e Decisões Técnicas

O projeto foi modelado utilizando conceitos de banco de dados orientado a documentos, visando flexibilidade e escalabilidade para a operação hoteleira:

* 🧠 **Modelagem Híbrida**: Uso estratégico de documentos embutidos (como endereços e preferências de hóspedes) para performance e referências com *snapshots* em reservas para manter a integridade histórica dos preços e dados.
* 🛠️ **Normalização Seletiva**: Coleções separadas para `hospedes`, `quartos`, `reservas`, `hospedagens`, `pagamentos`, `funcionarios`, `servicos` e `feedbacks`, permitindo consultas independentes e relatórios gerenciais otimizados.
* 🔐 **Gestão de Operação**: Estruturação de permissões de sistema e turnos dentro da coleção de funcionários para controle de acesso granular.

## 🔌 Coleções e Modelagem

### 1. Hóspedes e Quartos
* **Hóspedes**: Armazena dados cadastrais, preferências de estadia (como andar alto ou tipo de cama) e histórico de fidelidade.
* **Quartos**: Detalha a infraestrutura, categorias (Standard, Luxo, Presidencial), comodidades e status de manutenção/limpeza em tempo real.

### 2. Reservas e Hospedagens
* **Reservas**: Registro de intenção de estadia com snapshots dos dados do hóspede e do quarto para evitar inconsistências em caso de alterações futuras no cadastro.
* **Hospedagens**: Gerencia o período real da estadia, incluindo check-in/out e o consumo detalhado de serviços (frigobar, lavanderia, spa).

### 3. Financeiro e Feedback
* **Pagamentos**: Controle de transações, métodos de pagamento (cartão, PIX, faturamento corporativo) e emissão de documentos fiscais.
* **Feedbacks**: Avaliações detalhadas por categorias (limpeza, atendimento, conforto) e o registro de respostas oficiais do hotel.

## 💻 Tecnologias e Ferramentas Utilizadas
* 📄 **JSON**
* 🍃 **MongoDB Logic**
* 💻 **VSCode**
* 🐙 **Git e GitHub**

## 🎯 Objetivo
Este projeto foi desenvolvido para organizar o ecossistema de dados do Hotel Tasokare, eliminando a dispersão de informações em planilhas e papéis. O foco principal foi criar uma arquitetura flexível que suporte desde operações básicas de check-in até relatórios complexos de faturamento e ocupação.

---
👨‍💻 **Desenvolvido por Diogo Melo**
