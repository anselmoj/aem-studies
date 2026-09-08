## Manage Permissions for Folders

Aborda as regras de segurança baseadas em funções dentro do repositório de mídias

- **As Quatro Permissões Fundamentais**:
  1.  **Can View**: Acesso de leitura. Permite navegar pelas pastas, visualizar previews, fazer download, copiar ativos e compartilhar links.
  2.  **Can Edit**: Tudo de "Can View" + privilégios de alteração (criar e remover pastas; criar, atualizar, renomear, mover e remover ativos).
  3.  **Owner**: Tudo de "Can Edit" + capacidade de gerenciar e delegar permissões de pastas e suas subpastas para outros usuários.
  4.  **Deny Access**: Remove qualquer nível de permissão (View, Edit ou Owner).

- **Regra de ouro**:
  - **Sempre gerencie permissões para Grupos de Usuários (User Groups) e NUNCA para usuários individuais!**
  - A permissão **Deny Access** é suportada estritamente para Grupos de Usuários e deve ser usada com muita moderação (_use Deny Access sparingly_)
