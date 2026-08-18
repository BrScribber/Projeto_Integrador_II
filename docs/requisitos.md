# 📋 Documento de Engenharia de Requisitos

> **Projeto:** Sistema de Agendamento de Monitorias Acadêmicas  
> **Documento:** Especificação de Escopo e Requisitos  
> **Versão:** 1.0.0  
> **Status:** 🟢 Aprovado para Desenvolvimento Inicial  

---

## 🎯 1. Visão Geral do Escopo

O **Sistema de Agendamento de Monitorias Acadêmicas** visa resolver o problema da descentralização nos agendamentos de aulas de apoio universitário. A plataforma centraliza agendas, elimina conflitos de horários e gera histórico de atendimentos acadêmicos.

### 👥 Perfis de Usuário (Atores)
* **🎓 Aluno:** Busca monitorias disponíveis por disciplina, realiza e gerencia seus agendamentos.
* **🧑‍🏫 Monitor:** Cadastra disponibilidades de horários, confirma presenças e conclui atendimentos.
* **🛡️ Administrador/Coordenador:** Gestão geral do sistema (opcional em versões futuras).

---

## ⚡ 2. Requisitos Funcionais (RF)

| ID | Módulo | Descrição do Requisito | Prioridade |
| :---: | :--- | :--- | :---: |
| **RF01** | Autenticação | Permitir cadastro e login de Alunos e Monitores via e-mail institucional. | 🔴 Alta |
| **RF02** | Agenda | Permitir que o monitor cadastre, edite e remova seus horários vagos por disciplina. | 🔴 Alta |
| **RF03** | Busca | Disponibilizar busca de monitorias com filtros por nome da disciplina ou nome do monitor. | 🔴 Alta |
| **RF04** | Agendamento | Permitir ao aluno agendar um horário disponível com um clique. | 🔴 Alta |
| **RF05** | Cancelamento | Permitir o cancelamento do agendamento por qualquer uma das partes envolvidas. | 🟡 Média |
| **RF06** | Gestão de Status | Permitir que o monitor marque o atendimento como: *Pendente*, *Concluído* ou *Falta*. | 🟡 Média |
| **RF07** | Histórico | Exibir para o aluno e para o monitor o histórico completo de atendimentos passados. | 🟢 Baixa |
| **RF08** | Notificações | Exibir avisos e confirmações na tela ao realizar agendamentos ou cancelamentos. | 🟡 Média |

---

## 🛡️ 3. Requisitos Não-Funcionais (RNF)

| ID | Categoria | Descrição Detalhada | Prioridade |
| :---: | :--- | :--- | :---: |
| **RNF01** | **Usabilidade** | Interface Web responsiva (Mobile-First), adaptando-se a telas de smartphones e desktops. | 🔴 Alta |
| **RNF02** | **Desempenho** | O tempo de resposta para listagem de horários e confirmação não deve exceder 2 segundos. | 🟡 Média |
| **RNF03** | **Segurança** | Criptografia de senhas em banco de dados e proteção contra acessos não autorizados às agendas. | 🔴 Alta |
| **RNF04** | **Compatibilidade** | O sistema deve funcionar nos principais navegadores modernos (Chrome, Firefox, Edge, Safari). | 🔴 Alta |
| **RNF05** | **Documentação** | Código e documentação organizados no GitHub seguindo a convenção Markdown. | 🔴 Alta |

---

## ⚖️ 4. Regras de Negócio (RN)

As Regras de Negócio definem as restrições operacionais da aplicação:

* **RN01 - Antecedência para Cancelamento:** O cancelamento de um agendamento só é permitido com no mínimo **2 horas de antecedência** em relação ao horário marcado.
* **RN02 - Conflito de Horários:** O sistema não deve permitir que um aluno agende duas monitorias no mesmo dia e horário.
* **RN03 - Vagas Únicas:** Cada bloco de horário de monitoria só pode ser reservado por **1 aluno por vez** (atendimento individual).
