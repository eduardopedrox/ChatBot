# Agenda Escolar Inteligente

Uma agenda digital simples e prática para estudantes, com calendário interativo e integração com um chatbot inteligente para cadastro de tarefas por voz ou texto.

---

## Objetivo do Projeto

Criar uma agenda escolar web que ajude o aluno a organizar suas tarefas diárias de forma prática, com foco em:

- Visualização clara do calendário mensal.
- Registro de tarefas por dia diretamente no calendário.
- Integração com um chatbot (Landbot) para cadastro de tarefas de forma conversacional.

O diferencial está na integração com o chatbot, permitindo que o usuário diga coisas como “amanhã tenho prova de matemática” e a tarefa seja automaticamente criada na agenda.

---

## Tecnologias Utilizadas

- Frontend:
  - HTML5
  - CSS3 (com layout responsivo e gradientes suaves)
  - JavaScript (puro, sem frameworks)
- Armazenamento:
  - localStorage do navegador para salvar tarefas por data
- Chatbot:
  - Landbot (versão 3) para o chat fixo na tela
  - Integração via postMessage para receber tarefas do chatbot

---

## Funcionalidades Principais

1. Calendário Interativo
- Navegação entre meses com botões “◀” e “▶”.
- Visualização dos dias do mês em grade.
- Ícone de tarefa (📌) nos dias que possuem tarefas.
- Clique no dia para abrir o formulário de tarefas.

2. Registro de Tarefas
- Área de texto para escrever a tarefa do dia.
- Botão “Salvar Tarefa” que grava no localStorage.
- Atualização automática do calendário após salvar.

3. Integração com Chatbot (Landbot)
- Chatbot fixo no canto inferior direito da tela.
- O chatbot entende frases como:
  - “Amanhã tenho prova de matemática”
  - “Sexta-feira preciso entregar o trabalho de história”
- Ao identificar uma data e uma tarefa, o bot envia uma mensagem para a agenda via postMessage.
- A agenda recebe a mensagem, extrai a data e a descrição, e salva automaticamente no dia correspondente.

---

## Como Funciona a Integração com o Chatbot

A comunicação entre o Landbot e a agenda é feita via window.postMessage, seguindo este fluxo:

1. O usuário conversa com o chatbot e menciona uma tarefa com data.
2. O chatbot (configurado no painel Landbot) envia uma mensagem do tipo com a data e descrição.
3. A agenda escuta eventos message, salva a tarefa no localStorage e atualiza o calendário.
4. O calendário mostra um ícone indicando que o dia tem tarefa.

---

## Design e UX

- Paleta de cores com gradientes suaves (roxo/azul) para um visual moderno e acolhedor.
- Layout responsivo com max-width e padding adequados para telas pequenas.
- Botões com hover e feedback visual ao clicar.
- Chatbot fixo e sempre acessível, sem atrapalhar a navegação.

---

## Como Executar o Projeto

1. Baixe os arquivos: index.html, style.css e script.js.
2. Abra o arquivo index.html no navegador.
3. A agenda será carregada com o calendário atual e o chatbot já integrado.

> Observação: As tarefas são salvas localmente no navegador (localStorage).

---

## Estrutura de Arquivos

agenda-escolar/
├── index.html # Página principal com HTML
├── style.css # Estilos da agenda
├── script.js # Lógica do calendário e integração com Landbot
└── README.md # Documentação do projeto


---

## Possíveis Melhorias Futuras

- Sincronização com backend para salvar tarefas na nuvem.
- Suporte a lembretes por notificação.
- Exportar tarefas para PDF ou Google Calendar.
- Permitir múltiplas tarefas por dia.
- Adicionar autenticação para usuários.

---

## Licença

Projeto de código aberto para fins educacionais.  
© 2025 Agenda Escolar Inteligente. Todos os direitos reservados.
