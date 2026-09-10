## AEM Users, Groups, Permissions & ACLs

O documento detalha o modelo de segurança do AEM, destacando que o acesso é controlado por **duas camadas independentes e obrigatórias**:

1. **Adobe Admin Console (Product Profiles)**: Concede o direito técnico de licenciamento para acessar o ambiente AEM (ex: Power User, Collaborator, Limited User, Admin).

2. **AEM-local Group Membership e ACLs**: Define o que o usuário pode fazer dentro do sistema (ex: criar, editar, deletar, aprovar).
   - _Atenção de Prova_: O Admin Console sozinho não garante ações se o usuário não estiver no grupo local do AEM; da mesma forma, estar no grupo local não funciona se o usuário não tiver um Product Profile atribuído no Admin Console.

3. **Permissões Obrigatórias para Operações Comuns**:
   - **Upload de mídias**: Exige `rep:write` no caminho do DAM (`/content/dam`).
   - **Navegação e Busca no DAM:**: Exige leitura em `/content/dam` e privilégio `jcr:read` no caminho de esquemas de metadados (`/conf/global/settings/dam/adminui-extension/metadataschema`). Se o usuário não tiver acesso à pasta /conf, a interface falha com erro _NullPointerException_.
   - **Criar/Editar Folder Profiles**: Exige ser membro do grupo local de **administradores**.

4. **Avaliação de Regras e "Deny Wins"**:
   - O AEM avalia a árvore de permissões de baixo para cima (bottom-up).
   - **Regras de negação explicita (Deny) sempre vencem as regras de permissão (Allow)**, independente da ordem.
   - _Regra de Ouro_: Atribua permissões **sempre a Grupos de Usuários** (nunca a usuários individuais), priorize permissões _Allow_ e use _Deny_ com extrema moderação.
