# 🎓 Sistema de Agendamento de Monitorias Acadêmicas

> **Disciplina:** Projeto Integrador II  
> **Instituição:** Colégio Técnico de Bom Jesus (CTBJ / UFPI)  
> **Docente:** Prof. Clécio Sousa  
> **Discente:** André Barbosa de Oliveira  
> **Versão Oficial:** `v1.0.0`

---

## 🚀 Acesso Rápido ao Projeto

* 🌐 **Aplicação Online (GitHub Pages):** [Acessar Sistema de Monitorias Online](https://brscribber.github.io/Projeto_Integrador_II/)[cite: 2]
* 🎥 **Vídeo de Demonstração (YouTube):** [Assistir Vídeo Curto de Apresentação](https://youtube.com/shorts/jIAAni0sMlg)[cite: 2]
* 📋 **Quadro de Gestão Ágil (Notion):** [Acessar Kanban no Notion](/docs/Link%20Notion)[cite: 2, 3]

---

## 📌 Visão Geral e Justificativa

O **Sistema de Agendamento de Monitorias Acadêmicas** é uma solução web desenvolvida para centralizar e otimizar o fluxo de apoio pedagógico entre monitores e estudantes no ambiente escolar e acadêmico[cite: 1]. A plataforma substitui agendamentos informais por uma interface web minimalista, garantindo organização, persistência de dados e controle de horários em tempo real[cite: 1, 2].

---

## ✨ Principais Funcionalidades

* **Disciplinas Expandidas:** Suporte a matérias do currículo técnico e do Ensino Médio (Matemática, Língua Portuguesa, Física, Química, Biologia, História, Geografia, Inglês, Filosofia, Sociologia e Algoritmos/Informática).
* **Calendário Inteligente:** Seleção de data e horário com trava dinâmica em JavaScript que bloqueia a escolha de dias retroativos (passados).
* **Validação de Cadastro:** Validação rígida por expressão regular (Regex) exigindo Nome Completo e E-mail Institucional ou Matrícula (6 a 12 dígitos).
* **Persistência via LocalStorage:** Armazenamento local dos agendamentos no navegador (`Web Storage API`), garantindo que os dados permaneçam salvos após recarregar a página[cite: 2].
* **Cancelamento de Sessões:** Possibilidade de remover pedidos de monitoria do painel instantaneamente.
* **Design Minimalista & Responsivo:** Interface desenvolvida em CSS Grid e Flexbox com abordagem *Mobile-First*, adaptando-se a celulares e computadores.

---

## 📂 Estrutura de Documentação do Repositório

O repositório encontra-se organizado com todos os artefatos exigidos ao longo das três etapas da disciplina:

* 📜 **[Especificação de Requisitos (`/docs/requisitos.md`)](/docs/requisitos.md):** Requisitos Funcionais (RF), Não-Funcionais (RNF) e Regras de Negócio (RN)[cite: 1, 3].
* 🏗️ **[Relatório de Arquitetura (`/docs/arquitetura.md`)](/docs/arquitetura.md):** Diagramas em Mermaid.js (Sequência e ER) e Wireframe técnico[cite: 2, 3].
* 🧪 **[Relatório de Testes (`/docs/testes.md`)](/docs/testes.md):** Matriz de validação dos cenários de software e avaliação de usabilidade[cite: 2, 3].
* 📸 **[Diretório de Evidências (`/docs/evidencias.md`)](/docs/evidencias.md):** Detalhes do deploy no GitHub Pages, fotos/prints do LocalStorage no DevTools e links[cite: 2, 3].
* 💻 **[Código-Fonte (`/src/index.html`)](/src/index.html):** Código completo da aplicação web[cite: 2, 3].

---

## 🎥 Demonstração do Sistema em Vídeo

Clique na imagem abaixo ou no link para assistir à demonstração prática da aplicação:

[![Demonstração do Sistema no YouTube](https://img.youtube.com/vi/jIAAni0sMlg/hqdefault.jpg)](https://youtube.com/shorts/jIAAni0sMlg)

> 🔗 *Caso a capa não carregue, [clique aqui para assistir diretamente no YouTube Shorts](https://youtube.com/shorts/jIAAni0sMlg).*[cite: 2]

---

## 💻 Como Executar o Projeto Localmente

1. Clone o repositório para o seu computador:
   ```bash
   git clone [https://github.com/BrScribber/Projeto_Integrador_II.git](https://github.com/BrScribber/Projeto_Integrador_II.git)
