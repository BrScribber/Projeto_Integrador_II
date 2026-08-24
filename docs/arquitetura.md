# 🏗️ Relatório de Arquitetura e Modelagem do Sistema

> **Projeto:** Sistema de Agendamento de Monitorias Acadêmicas  
> **Fase:** Etapa 2 - Planejamento Operacional e Modelagem  
> **Status:** 🟢 Concluído  

---

## 📐 1. Diagrama de Fluxo de Agendamento

O diagrama abaixo ilustra o fluxo de interação entre o **Aluno**, a **Interface (Frontend)** e a **Base de Dados** ao agendar uma monitoria.

```mermaid
sequenceDiagram
    autonumber
    actor Aluno
    participant Sistema as Interface Web
    participant Banco as Banco de Dados

    Aluno->>Sistema: Seleciona Disciplina e Monitor
    Sistema->>Banco: Consulta horários livres
    Banco-->>Sistema: Retorna horários disponíveis
    Aluno->>Sistema: Confirma agendamento no horário desejado
    Sistema->>Banco: Valida se horário continua vago (RN03)
    alt Horário Livre
        Banco-->>Sistema: Registra agendamento com status "Pendente"
        Sistema-->>Aluno: Exibe mensagem "Agendamento Realizado!"
    else Horário Ocupado
        Banco-->>Sistema: Retorna erro de conflito
        Sistema-->>Aluno: Exibe mensagem "Horário não mais disponível"
    end
