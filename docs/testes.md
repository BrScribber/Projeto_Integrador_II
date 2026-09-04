# 🧪 Relatório de Validação e Testes de Software

> **Projeto:** Sistema de Agendamento de Monitorias Acadêmicas  
> **Artefato:** /docs/testes.md  
> **Data:** 27/08/2026  

---

## 📌 1. Escopo da Validação
Este documento reúne a matriz de testes funcionais executados no protótipo web completo, validando persistência de dados local, regras de validação de formulário (Regex) e responsividade da interface minimalista.

---

## 📊 2. Matriz de Testes Executados

| ID | Cenário / Caso de Teste | Requisito | Resultado Esperado | Resultado Obtido | Status |
| :---: | :--- | :---: | :--- | :--- | :---: |
| **TC01** | Submissão de agendamento válido. | `RF04` | Salvar o agendamento no painel e exibir notificação Toast. | Agendamento listado e Toast exibido por 3 segundos. | 🟢 Aprovado |
| **TC02** | Validação de Nome Completo e E-mail/Matrícula. | `RF01` / `RNF03` | Impedir envio se o nome não for completo ou a matrícula/e-mail for inválido. | Exibição de bordas vermelhas e mensagens de erro específicas. | 🟢 Aprovado |
| **TC03** | Seleção de data no calendário. | `RN01` | Bloquear a seleção de dias passados no input de data. | Atributo `min` aplicado dinamicamente com a data atual. | 🟢 Aprovado |
| **TC04** | Cancelamento e remoção de monitoria. | `RF05` | Excluir o card do agendamento imediatamente ao clicar em "Cancelar". | Item removido da lista e atualizado na memória do navegador. | 🟢 Aprovado |
| **TC05** | Persistência de dados via LocalStorage. | `RNF02` | Manter a lista de agendamentos intacta após atualizar a página (F5). | Dados recarregados automaticamente via `DOMContentLoaded`. | 🟢 Aprovado |
| **TC06** | Teste de responsividade e acessibilidade. | `RNF01` | Adequação do layout em telas mobile e suporte a contraste/leitores. | Layout ajustado perfeitamente via CSS Grid/Flexbox e foco acessível. | 🟢 Aprovado |

---

## 🗣️ 3. Feedback da Validação com Usuários Reais

* **Estudante (Usuário Aluno):** *"A possibilidade de cancelar o agendamento e a validação do e-mail institucional trouxeram muito mais segurança para o uso no dia a dia."*
* **Monitor (Usuário Administrador):** *"O design ficou muito limpo e intuitivo. O filtro automático de datas passadas evita confusões de horário."*
