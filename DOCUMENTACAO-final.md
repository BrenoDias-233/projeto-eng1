
# DOCUMENTAÇÃO

## Requisitos Funcionais (RF)

| Código | Descrição |
|--------|-----------|
| RF01 | O sistema deve permitir a criação de uma conta com nome, e-mail e senha. |
| RF02 | O sistema deve autenticar usuários para que acessem a plataforma utilizando e-mail e senha válidos. |
| RF03 | O usuário deve poder criar projetos com nome e descrição. |
| RF04 | O usuário deve ser capaz de excluir os projetos criados. |
| RF05 | O sistema deve permitir a criação de tarefas em um projeto, contendo título, descrição, responsável (opcional), status e data de criação. |
| RF06 | O usuário deve ser capaz de atribuir uma tarefa a um membro do projeto. |
| RF07 | O sistema deve permitir a alteração ou exclusão das tarefas existentes. |
| RF08 | O sistema deve classificar o status das tarefas entre: a fazer, em progresso e concluído. |
| RF09 | O sistema deve permitir a criação de comentários nas tarefas. |
| RF10 | O sistema deve gerar notificações em eventos como atribuição de tarefas, mudança de status, novos comentários, entrada de novo membro no projeto, nova tarefa atribuída, novo comentário em tarefa atribuída ao usuário e mudanças de status. |
| RF11 | O sistema deve registrar e apresentar um histórico contendo alterações de status, mudanças de responsáveis e edições em tarefas. |

## Requisitos Não Funcionais (RNF)

| Código | Descrição |
|--------|-----------|
| RNF01 | O sistema deve ser intuitivo e de fácil aprendizado. |
| RNF02 | O sistema deve ser compatível com os navegadores mais populares do mercado. |
| RNF03 | O sistema deve realizar logout automático após 1 hora de inatividade. |

## 2. Cartões XP

| Cartão | Descrição | Critérios |
|--------|-----------|-----------|
| Criar conta | Como visitante, quero criar uma conta para acessar a plataforma e participar de projetos. | Cadastro usa nome, e-mail e senha; e-mail deve ser único; senha deve atender aos critérios mínimos definidos. |
| Autenticação de usuário | Como usuário registrado quero fazer login com e-mail e senha para acessar meus projetos e tarefas. | E-mail e senha devem ser validados. |
| Criar projeto | Como usuário, quero criar projetos para organizar tarefas do meu grupo. | Nome é obrigatório; a descrição é opcional. |
| Excluir projeto | Como criador do projeto, quero poder excluir para remover informações não mais úteis. | Exibir aviso de confirmação; tarefas do projeto devem ser excluídas. |
| Criar tarefas | Como membro do projeto, quero criar tarefas para organizar e registrar atividades. | Deve conter título, descrição, responsável (opcional), status e data de criação; status inicial = A Fazer. |
| Atribuir tarefa a membro | Como usuário, quero atribuir uma tarefa a um membro para distribuir responsabilidades dentro da equipe. | Alteração deve gerar notificação; apenas o dono do projeto pode atribuir tarefas. |
| Editar e excluir tarefas | Como usuário, quero editar ou excluir tarefas para mantê-las atualizadas ou remover tarefas não úteis. | Apenas usuários autorizados podem editar/excluir; exclusão deve pedir confirmação; alterações devem ser notificadas. |
| Alterar status da tarefa | Como membro do projeto, quero alterar o status das tarefas para indicar seu andamento. | Mudanças registradas no histórico; deve gerar notificação. |
| Criar comentários em tarefas | Como membro do projeto, quero comentar em tarefas para compartilhar informações. | Comentários devem exibir autor e data. |
| Notificações | Como usuário, quero receber notificações sobre eventos para acompanhar mudanças no projeto. | Eventos: atribuição de tarefas; mudança de status; novos comentários; nova tarefa criada. |
| Histórico de Alterações | Como usuário, quero ter acesso ao histórico de uma tarefa para entender o que mudou, quando e quem fez. | Deve registrar mudanças de status; mudança de responsável; edições feitas. |

## 3. Spikes

### Spike 01 – Estudo sobre notificações em tempo real
Nós precisamos entender quais tecnologias são mais adequadas para implementar notificações em tempo real no sistema, já que os usuários devem receber atualizações instantâneas sobre tarefas, comentários e mudanças nos projetos. Vamos pesquisar opções como WebSockets, Socket.io, SSE e também soluções de push, como Firebase Cloud Messaging.

### Spike 02 – Análise de ferramentas para upload de arquivos
Antes de desenvolver a funcionalidade de envio de arquivos, vamos testar algumas ferramentas que permitam realizar uploads de forma segura e organizada.

### Spike 03 – Escolha do banco de dados ideal
[...]

### Spike 04 – Teste de ferramentas para criação dos mockups
[...]

### Spike 05 – Modelagem para organização de tarefas e tópicos
[...]

## 4. Mockups

- Tela 1 – Login  
- Tela 2 – Mural  
- Tela 3 – Tarefas  
- Tela 4 – Perfil  

## 5. Cronograma (Gantt)

| Fase | Atividade | Início | Fim | Duração |
|------|-----------|--------|------|----------|
| 1 | Levantamento do sistema | 01/11 | 03/11 | 3 dias |
| 2 | Definição de requisitos | 03/11 | 05/11 | 2 dias |
| 3 | Cartões XP | 05/11 | 06/11 | 1 dia |
| 4 | Spikes | 05/11 | 08/11 | 3 dias |
| 5 | Mockups | 08/11 | 11/11 | 3 dias |
| 6 | Repositório GitHub | 10/11 | 11/11 | 2 dias |
