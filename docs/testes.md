# 🧪 Relatório de Validação e Testes de Software

> **Projeto:** Sistema de Agendamento de Monitorias Acadêmicas  
> **Artefato:** /docs/testes.md  

---

## 📌 1. Escopo da Validação
Este documento reúne os resultados das simulações de testes funcionais e não-funcionais realizadas na interface web da aplicação, bem como a avaliação de usabilidade conduzida com usuários do contexto acadêmico.

---

## 📊 2. Matriz de Testes Executados

| ID | Cenário / Casos de Teste | Requisito | Resultado Esperado | Resultado Obtido | Status |
| :---: | :--- | :---: | :--- | :--- | :---: |
| **TC01** | Submissão do formulário com todos os dados preenchidos. | `RF04` | Registro do agendamento e exibição do alerta de confirmação. | Agendamento exibido no painel dinâmico e alerta exibido. | 🟢 Aprovado |
| **TC02** | Tentativa de envio com campo de e-mail/nome vazio. | `RF01` | Bloqueio nativo do formulário exigindo o preenchimento. | O navegador bloqueou o envio e indicou o campo pendente. | 🟢 Aprovado |
| **TC03** | Teste de responsividade da interface web em smartphones. | `RNF01` | Ajuste do layout sem quebra de texto ou botões fora da tela. | Formulário e botões adaptaram-se perfeitamente em 360px. | 🟢 Aprovado |
| **TC04** | Resposta da interface ao confirmar o agendamento. | `RNF02` | Tempo de confirmação visual inferior a 2 segundos. | Confirmação instantânea (0,1 segundo). | 🟢 Aprovado |

---

## 🗣️ 3. Feedback da Validação com Usuários Reais

* **Estudante (Usuário Aluno):** *"O formulário é direto ao ponto. Consegui escolher a disciplina e o horário em menos de 1 minuto sem precisar mandar mensagens no WhatsApp."*
* **Monitor (Usuário Administrador):** *"A visualização dos agendamentos logo abaixo do formulário ajuda a confirmar a reserva na hora."*
