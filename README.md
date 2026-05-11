<h1 align="center"><a href="./HotelNebula/Instructions/README.md" target="_blank">🏨 Hotel Nebula - Gestão Hoteleira</a></h1>

<img width="2752" height="1536" alt="A_wide_16_9_202604221302" src="https://github.com/user-attachments/assets/27ad1b2f-b5d0-454e-a9ac-2feb4d2fca7c" />
<br>

Projeto de estruturação e modelagem de um banco de dados não relacional (NoSQL) para a gestão completa da rede hoteleira Hotel Nebula. O objetivo é organizar digitalmente os dados dispersos para melhorar reservas, hospedagens, serviços, avaliações e gestão financeira, preparando o terreno para uma futura API.

---

## 🚀 Etapas do Projeto

O desenvolvimento foi dividido em três partes principais:
* **Parte 1: Origem do Sistema** - Identificação dos núcleos de informação, definição das coleções, decisão sobre documentos embutidos vs. referenciados e desenho do esquema inicial (modelagem estrutural).
* **Parte 2: Montagem do Núcleo** - Implementação física no banco NoSQL, criação das coleções e inserção de documentos de exemplo (hóspedes, quartos, funcionários, serviços, etc) com dados aninhados.
* **Parte 3: Radar de Comando** - Produção de consultas (queries) estratégicas para a gestão do hotel, respondendo perguntas de negócio como ocupação, faturamento e fidelidade de hóspedes.

---

## � Estrutura do Projeto e Decisões Técnicas

O projeto foi modelado utilizando conceitos de banco de dados orientado a documentos, visando flexibilidade e escalabilidade para a operação hoteleira:

* 🧠 **Modelagem Híbrida**: Uso estratégico de documentos embutidos (como endereços e preferências de hóspedes, turnos de funcionários) para performance e referências com *snapshots* em reservas para manter a integridade histórica dos preços e dados cadastrais.
* 🛠️ **Normalização Seletiva**: Foram definidas 8 coleções principais: `hospedes`, `quartos`, `reservas`, `hospedagens`, `pagamentos`, `funcionarios`, `servicos` e `feedbacks`, permitindo consultas independentes.
* 📊 **Consultas Gerenciais**: Estrutura de schema e subdocumentos projetada para facilitar as agregações complexas da "Parte 3", simplificando agrupamentos para faturamento e busca de características.

## 🔌 Coleções e Modelagem

### 1. Hóspedes e Quartos
* **Hóspedes**: Armazena dados cadastrais, preferências de estadia (como andar alto ou tipo de cama) e histórico de fidelidade.
* **Quartos**: Detalha a infraestrutura, categorias (Standard, Luxo, Presidencial), comodidades e status de manutenção/limpeza em tempo real.

### 2. Reservas e Hospedagens
* **Reservas**: Registro de intenção de estadia com snapshots dos dados do hóspede e do quarto para evitar inconsistências em caso de alterações futuras no cadastro.
* **Hospedagens**: Gerencia o período real da estadia, incluindo check-in/out e o consumo detalhado de serviços, que são embutidos como subdocumentos na estadia.

### 3. Financeiro, Funcionários e Feedback
* **Pagamentos**: Controle de transações vinculadas à hospedagem, com suporte a múltiplas parcelas e métodos de pagamento integrados.
* **Feedbacks**: Avaliações detalhadas por categorias (limpeza, atendimento, conforto) e o registro de respostas oficiais do hotel.
* **Funcionários** e **Serviços**: Gestão de pessoal com alocação e controle de acesso, além do catálogo isolado de serviços disponíveis no hotel.

## 💻 Tecnologias e Ferramentas Utilizadas
* 📄 **JSON**
* 🍃 **MongoDB Logic**
* 💻 **VSCode**
* 🐙 **Git e GitHub**

---
👨‍💻 **Desenvolvido por Diogo Melo**
