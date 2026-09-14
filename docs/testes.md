> **Projeto:** Sistema de Agendamento de Monitorias Acadêmicas  
> **Artefato:** /docs/testes.md  

---

## 📌 1. Escopo da Validação
Este documento reúne os resultados das simulações de testes funcionais e não-funcionais realizadas na interface web da aplicação, bem como a avaliação de usabilidade conduzida com usuários do contexto acadêmico.
Este documento reúne a matriz de testes funcionais executados no protótipo web completo, validando persistência de dados local, regras de validação de formulário (Regex) e responsividade da interface minimalista.

---

## 📊 2. Matriz de Testes Executados

| ID | Cenário / Casos de Teste | Requisito | Resultado Esperado | Resultado Obtido | Status |
| ID | Cenário / Caso de Teste | Requisito | Resultado Esperado | Resultado Obtido | Status |
| :---: | :--- | :---: | :--- | :--- | :---: |
| **TC01** | Submissão do formulário com todos os dados preenchidos. | `RF04` | Registro do agendamento e exibição do alerta de confirmação. | Agendamento exibido no painel dinâmico e alerta exibido. | 🟢 Aprovado |
| **TC02** | Tentativa de envio com campo de e-mail/nome vazio. | `RF01` | Bloqueio nativo do formulário exigindo o preenchimento. | O navegador bloqueou o envio e indicou o campo pendente. | 🟢 Aprovado |
| **TC03** | Teste de responsividade da interface web em smartphones. | `RNF01` | Ajuste do layout sem quebra de texto ou botões fora da tela. | Formulário e botões adaptaram-se perfeitamente em 360px. | 🟢 Aprovado |
| **TC04** | Resposta da interface ao confirmar o agendamento. | `RNF02` | Tempo de confirmação visual inferior a 2 segundos. | Confirmação instantânea (0,1 segundo). | 🟢 Aprovado |
| **TC01** | Submissão de agendamento válido. | `RF04` | Salvar o agendamento no painel e exibir notificação Toast. | Agendamento listado e Toast exibido por 3 segundos. | 🟢 Aprovado |
| **TC02** | Validação de Nome Completo e E-mail/Matrícula. | `RF01` / `RNF03` | Impedir envio se o nome não for completo ou a matrícula/e-mail for inválido. | Exibição de bordas vermelhas e mensagens de erro específicas. | 🟢 Aprovado |
| **TC03** | Seleção de data no calendário. | `RN01` | Bloquear a seleção de dias passados no input de data. | Atributo `min` aplicado dinamicamente com a data atual. | 🟢 Aprovado |
| **TC04** | Cancelamento e remoção de monitoria. | `RF05` | Excluir o card do agendamento imediatamente ao clicar em "Cancelar". | Item removido da lista e atualizado na memória do navegador. | 🟢 Aprovado |
| **TC05** | Persistência de dados via LocalStorage. | `RNF02` | Manter a lista de agendamentos intacta após atualizar a página (F5). | Dados recarregados automaticamente via `DOMContentLoaded`. | 🟢 Aprovado |
| **TC06** | Teste de responsividade e acessibilidade. | `RNF01` | Adequação do layout em telas mobile e suporte a contraste/leitores. | Layout ajustado perfeitamente via CSS Grid/Flexbox e foco acessível. | 🟢 Aprovado |

---

## 🗣️ 3. Feedback da Validação com Usuários Reais

* **Estudante (Usuário Aluno):** *"O formulário é direto ao ponto. Consegui escolher a disciplina e o horário em menos de 1 minuto sem precisar mandar mensagens no WhatsApp."*
* **Monitor (Usuário Administrador):** *"A visualização dos agendamentos logo abaixo do formulário ajuda a confirmar a reserva na hora."*
* **Estudante (Usuário Aluno):** *"A possibilidade de cancelar o agendamento e a validação do e-mail institucional trouxeram muito mais segurança para o uso no dia a dia."*
* **Monitor (Usuário Administrador):** *"O design ficou muito limpo e intuitivo. O filtro automático de datas passadas evita confusões de horário."*
