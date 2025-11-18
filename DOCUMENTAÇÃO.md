**Requisitos Funcionais (RF)**

  ---------------------------------------------------------------------
  Código   Descrição
  -------- ------------------------------------------------------------
  RF01     O sistema deve permitir a criação de uma conta com nome,
           e-mail e senha.

  RF02     O sistema deve autenticar usuários para que acessem a
           plataforma utilizando e-mail e senha válidos.

  RF03     O usuário deve poder criar projetos com nome e descrição.

  RF04     O usuário deve ser capaz de excluir os projetos criados.

  RF05     O sistema deve permitir a criação de tarefas em um projeto,
           contendo título, descrição, responsável (opcional), status e
           data de criação

  RF06     O usuário deve ser capaz de atribuir uma tarefa a um membro
           do projeto.

  RF07     O sistema deve permitir a alteração ou exclusão das tarefas
           existentes.

  RF08     O sistema deve classificar o status das tarefas entre: a
           fazer, em progresso e concluído

  RF09     O sistema deve permitir a criação de comentários nas
           tarefas.

  RF10     O sistema deve gerar notificações em eventos como atribuição
           de tarefas, mudança de status, novos comentários, entrada de
           novo membro no projeto, nova tarefa atribuída, novo
           comentário em tarefa atribuída ao usuário e mudanças de
           status

  RF11     O sistema deve registrar e apresentar um histórico contendo
           alterações de status, mudanças de responsáveis e edições em
           tarefas.
  ---------------------------------------------------------------------

**Requisitos Não-Funcionais (RNF)**

  ---------------------------------------------------------------------
  Código   Descrição
  -------- ------------------------------------------------------------
  RNF01    O sistema deve ser intuitivo e de fácil aprendizado.

  RNF02    O sistema deve ser compatível com os navegadores mais
           populares do mercado.

  RNF03    O sistema deve realizar logout automático após 1 hora de
           inatividade.
  ---------------------------------------------------------------------

**2. Cartões XP**

+----------------------+----------------------+------------------------+
| Cartão               | Descrição            | Critérios              |
+======================+======================+========================+
| Criar conta          | Como visitante,      | Cadastro usa nome,     |
|                      | quero criar uma      | e-mail e senha         |
|                      | conta para acessar a |                        |
|                      | plataforma e         | O e-mail deve ser      |
|                      | participar de        | único no sistema;      |
|                      | projetos.            |                        |
|                      |                      | A senha deve atender   |
|                      |                      | aos critérios mínimos  |
|                      |                      | definidos.             |
+----------------------+----------------------+------------------------+
| Autenticação de      | Como usuário         | E-mail e senha devem   |
| usuário              | registrado quero     | ser validados          |
|                      | fazer login com      |                        |
|                      | e-mail e senha para  |                        |
|                      | acessar meus         |                        |
|                      | projetos e tarefas.  |                        |
+----------------------+----------------------+------------------------+
| Criar projeto        | Como usuário, quero  | Nome é obrigatório;    |
|                      | criar projetos para  |                        |
|                      | organizar tarefas do | A descrição é          |
|                      | meu grupo            | opcional.              |
+----------------------+----------------------+------------------------+
| Excluir projeto      | Como criador do      | Exibir aviso de        |
|                      | projeto, quero poder | confirmação;           |
|                      | excluir para remover |                        |
|                      | informações não mais | Tarefas do projeto     |
|                      | úteis                | devem ser excluidas.   |
+----------------------+----------------------+------------------------+
| Criar tarefas        | Como membro do       | Deve conter título,    |
|                      | projeto, quero criar | descrição, responsável |
|                      | tarefas para         | (opcional), status e   |
|                      | organizar e          | data de criação;       |
|                      | registrar            |                        |
|                      | atividades.          | Status inicial = A     |
|                      |                      | Fazer.                 |
+----------------------+----------------------+------------------------+
| Atribuir tarefa a    | Como usuário, quero  | A alteração deve gerar |
| membro               | atribuir uma tarefa  | notificação;           |
|                      | a um membro para     |                        |
|                      | distribuir           | Apenas o dono do       |
|                      | responsabilidades    | projeto pode atribuir  |
|                      | dentro da equipe.    | tarefas.               |
+----------------------+----------------------+------------------------+
| Editar e excluir     | Como usuário, quero  | Apenas usuários        |
| tarefas              | editar ou excluir    | autorizados podem      |
|                      | tarefas para         | editar/excluir;        |
|                      | mantê-las            |                        |
|                      | atualizadas ou       | Exclusão deve pedir    |
|                      | remover tarefas não  | confirmação;           |
|                      | úteis.               |                        |
|                      |                      | Alterações devem ser   |
|                      |                      | notificadas.           |
+----------------------+----------------------+------------------------+
| Alterar status da    | Como membro do       | Mudanças de status     |
| tarefa               | projeto, quero       | registradas no         |
|                      | alterar o status das | histórico;             |
|                      | tarefas para indicar |                        |
|                      | seu andamento        | Deve gerar             |
|                      |                      | notificação;           |
+----------------------+----------------------+------------------------+
| Criar comentarios em | Como membro do       | Comentários devem      |
| tarefas              | projeto, quero       | exibir autor e data;   |
|                      | comentar em tarefas  |                        |
|                      | para compartilhar    |                        |
|                      | informações.         |                        |
+----------------------+----------------------+------------------------+
| Notificações         | Como usuário, quero  | Eventos que devem      |
|                      | receber notificações | gerar notificação:     |
|                      | sobre eventos para   |                        |
|                      | acompanhar mudanças  | Atribuição de tarefas; |
|                      | no projeto.          |                        |
|                      |                      | Mudança de status;     |
|                      |                      |                        |
|                      |                      | Novos comentários;     |
|                      |                      |                        |
|                      |                      | Nova tarefa criada.    |
+----------------------+----------------------+------------------------+
| Histórico de         | Como usuário, quero  | Histórico deve         |
| Alterações           | ter acesso ao        | registrar:             |
|                      | histórico de de uma  |                        |
|                      | tarefa para entender | Mudanças de status;    |
|                      | o que mudou, quando  |                        |
|                      | e quem fez.          | Mudança de             |
|                      |                      | responsável;           |
|                      |                      |                        |
|                      |                      | Edição de tarefas.     |
+----------------------+----------------------+------------------------+

**3. Spikes**

### **Spike 01 -- Estudo sobre notificações em tempo real**

Nós precisamos entender quais tecnologias são mais adequadas para
implementar notificações em tempo real no sistema, já que os usuários
devem receber atualizações instantâneas sobre tarefas, comentários e
mudanças nos projetos. Vamos pesquisar opções como WebSockets,
Socket.io, SSE e também soluções de push, como Firebase Cloud Messaging.
Nosso objetivo é identificar qual alternativa oferece melhor desempenho,
integra bem com o backend e o frontend escolhidos, e ainda permite
integrar notificações por e-mail, conforme os requisitos do projeto.

### **Spike 02 -- Análise de ferramentas para upload de arquivos**

Antes de desenvolver a funcionalidade de envio de arquivos, vamos testar
algumas ferramentas que permitam realizar uploads de forma segura e
organizada. Avaliaremos bibliotecas como Multer (caso utilizemos
Node.js) e serviços de armazenamento em nuvem, como Firebase Storage,
Supabase e AWS S3. Pretendemos comparar segurança, permissões,
facilidade de implementação e suporte a histórico de alterações, que é
algo previsto no projeto.

### **Spike 03 -- Escolha do banco de dados ideal**

Para armazenar usuários, projetos, tarefas, comentários, notificações e
o histórico de mudanças, vamos analisar diferentes bancos de dados
recomendados: PostgreSQL, MySQL, MongoDB e Firestore. O objetivo é
avaliar desempenho, flexibilidade da modelagem, suporte a consultas mais
complexas, integração com o backend e comportamento em cenários de uso
simultâneo. Ao final, escolheremos o banco mais adequado e
justificaremos tecnicamente a decisão.

### **Spike 04 -- Teste de ferramentas para criação dos mockups**

Antes de começar a desenhar as telas do sistema, vamos testar algumas
ferramentas de prototipação para identificar qual facilita mais o
trabalho do grupo. Entre as opções que iremos analisar estão Figma,
Canva e Balsamiq. Vamos comparar facilidade de uso, colaboração entre os
integrantes, qualidade da prototipação e recursos para documentar o
design de maneira clara e organizada.

### **Spike 05 -- Modelagem para organização de tarefas e tópicos**

Este spike tem como objetivo estudar a melhor forma de modelar a
organização de tarefas e tópicos de estudo dentro do sistema. Vamos
pesquisar estruturas de tabelas, tipos de relacionamentos e estratégias
de indexação que deixem as consultas mais eficientes. Também vamos
considerar as diferenças entre modelagens relacionais e NoSQL,
garantindo que a estrutura suporte múltiplos usuários colaborando ao
mesmo tempo sem perda de desempenho.

**5. Cronograma (Gantt)**

  ------------------------------------------------------------------------
  Fase           Atividade             Início     Fim       Duração
  -------------- --------------------- ---------- --------- --------------
  1              Levantamento do       01/11      03/11     3 dias
                 sistema                                    

  2              Definição de          03/11      05/11     2 dias
                 requisitos                                 

  3              Cartões XP            05/11      06/11     1 dia

  4              Spikes                05/11      08/11     3 dias

  5              Mockups               08/11      11/11     3 dias

  6              Repositório GitHub    10/11      11/11     2 dias
  ------------------------------------------------------------------------


| Cartão               | Descrição            | Critérios              |
| ---                  | ---                  |                     --- |
| Criar conta          | Como visitante,      | Cadastro usa nome,     |
|                      | quero criar uma      | e-mail e senha         |
|                      | conta para acessar a |                        |
|                      | plataforma e         | O e-mail deve ser      |
|                      | participar de        | único no sistema;      |
|                      | projetos.            |                        |
|                      |                      | A senha deve atender   |
|                      |                      | aos critérios mínimos  |
|                      |                      | definidos.             |

| Autenticação de      | Como usuário         | E-mail e senha devem   |
| usuário              | registrado quero     | ser validados          |
|                      | fazer login com      |                        |
|                      | e-mail e senha para  |                        |
|                      | acessar meus         |                        |
|                      | projetos e tarefas.  |                        |
+----------------------+----------------------+------------------------+
| Criar projeto        | Como usuário, quero  | Nome é obrigatório;    |
|                      | criar projetos para  |                        |
|                      | organizar tarefas do | A descrição é          |
|                      | meu grupo            | opcional.              |
+----------------------+----------------------+------------------------+
| Excluir projeto      | Como criador do      | Exibir aviso de        |
|                      | projeto, quero poder | confirmação;           |
|                      | excluir para remover |                        |
|                      | informações não mais | Tarefas do projeto     |
|                      | úteis                | devem ser excluidas.   |
+----------------------+----------------------+------------------------+
| Criar tarefas        | Como membro do       | Deve conter título,    |
|                      | projeto, quero criar | descrição, responsável |
|                      | tarefas para         | (opcional), status e   |
|                      | organizar e          | data de criação;       |
|                      | registrar            |                        |
|                      | atividades.          | Status inicial = A     |
|                      |                      | Fazer.                 |
+----------------------+----------------------+------------------------+
| Atribuir tarefa a    | Como usuário, quero  | A alteração deve gerar |
| membro               | atribuir uma tarefa  | notificação;           |
|                      | a um membro para     |                        |
|                      | distribuir           | Apenas o dono do       |
|                      | responsabilidades    | projeto pode atribuir  |
|                      | dentro da equipe.    | tarefas.               |
+----------------------+----------------------+------------------------+
| Editar e excluir     | Como usuário, quero  | Apenas usuários        |
| tarefas              | editar ou excluir    | autorizados podem      |
|                      | tarefas para         | editar/excluir;        |
|                      | mantê-las            |                        |
|                      | atualizadas ou       | Exclusão deve pedir    |
|                      | remover tarefas não  | confirmação;           |
|                      | úteis.               |                        |
|                      |                      | Alterações devem ser   |
|                      |                      | notificadas.           |
+----------------------+----------------------+------------------------+
| Alterar status da    | Como membro do       | Mudanças de status     |
| tarefa               | projeto, quero       | registradas no         |
|                      | alterar o status das | histórico;             |
|                      | tarefas para indicar |                        |
|                      | seu andamento        | Deve gerar             |
|                      |                      | notificação;           |
+----------------------+----------------------+------------------------+
| Criar comentarios em | Como membro do       | Comentários devem      |
| tarefas              | projeto, quero       | exibir autor e data;   |
|                      | comentar em tarefas  |                        |
|                      | para compartilhar    |                        |
|                      | informações.         |                        |
+----------------------+----------------------+------------------------+
| Notificações         | Como usuário, quero  | Eventos que devem      |
|                      | receber notificações | gerar notificação:     |
|                      | sobre eventos para   |                        |
|                      | acompanhar mudanças  | Atribuição de tarefas; |
|                      | no projeto.          |                        |
|                      |                      | Mudança de status;     |
|                      |                      |                        |
|                      |                      | Novos comentários;     |
|                      |                      |                        |
|                      |                      | Nova tarefa criada.    |
+----------------------+----------------------+------------------------+
| Histórico de         | Como usuário, quero  | Histórico deve         |
| Alterações           | ter acesso ao        | registrar:             |
|                      | histórico de de uma  |                        |
|                      | tarefa para entender | Mudanças de status;    |
|                      | o que mudou, quando  |                        |
|                      | e quem fez.          | Mudança de             |
|                      |                      | responsável;           |
|                      |                      |                        |
|                      |                      | Edição de tarefas.     |
+----------------------+----------------------+------------------------+
