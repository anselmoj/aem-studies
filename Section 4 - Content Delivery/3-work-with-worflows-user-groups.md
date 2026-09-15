## Work with Workflows &amp; User Groups (Automação e Vinculação de Grupos)

- **Vinculação de Grupos de Usuários e Etapas de Workflows**
  - Etapas de workflow que exigem ação humana (_Participant Steps_) são atribuídas a **Grupos de Usuários** (como `workflow-users` ou grupos do projeto).
  - Quando o fluxo atinge a etapa, a tarefa aparece na caixa de entrada (**Inbox**) de todos os membros do grupo. Qualquer membro pode assumir (_Complete_) ou delegar (_Delegate_) a tarefa.

- **Tipos Importantes de Participant Steps**:
  - **Participant Step**: Exige confirmação manual simples de um usuário/grupo.
  - **Dialog Participant Step**: Coleta dados do usuário através de um formulário/diálogo durante a aprovação e armazena os dados no _payload_ ou nos metadados do _work item_.
  - **Dynamic Participant Step**: Utiliza um _Participant Chooser_ (script ECMA ou serviço OSGi) para selecionar automaticamente o usuário correto em tempo de execução (ex: selecionar o criador do fluxo como aprovador).

- **Estruturas de Controle no WorkFlow**:
  - **AND Split**: Cria ramificações paralelas ativas simultaneamente (ex: revisão jurídica e revisão de design acontecendo ao mesmo tempo).
  - **OR Split**: Avalia regra/expressões e segue apenas pela primeira rota verdadeira.
  - **Goto Split**: Permite criar rotas avançadas ou loops de repetição.
