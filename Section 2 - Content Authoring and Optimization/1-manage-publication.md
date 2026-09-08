## Manage Publication

Este pilar lida com a governança e a transição de mídias de Author para o ambiente de entrega.

- **Quick Publish vs. Manage Publication**:
  - **Quick Publish**: Publica imediatamente os ativos ou pastas selecionados par ao destino padrão (AEM Assets)
  - **Manage Publication**: Interface avançada que permite: adicionar mídias de diferentes locais do DAM, incluir e filtrar configurações de pastas, e agendar a publicação para data/hora futura ("Publish Later")

- **Include Folder Settings**:
  - Se voce publicar uma pasta, por padrão, o AEM publica todos os ativos, subpastas e referências. No entanto, voce pode filtrar esse comportamento.
    - **Include folder contents (Habilitado)**: Sobe tudo (pastas, subpastas, ativos internos e referências)
    - **Include folder contents (Desabilitado)**: Sobe apenas a estrutura de pasta vazia e suas referências. Nenhum ativo interno é publicado

- **Níveis de Usuário e Permissões de Fluxo (Request Publication)**:
  - **Contributor**: Pode subir mídias, mas não tem permissão para publicar. O botão "Manage Publication" fica oculto para ele.
  - **Workflow User**: Não pode publicar diretamente, mas tem acesso de leitura ao workflow. Ele pode solicitar publicação ("Request Publication") e agendar agendamentos de disparo.
  - **Admin**: Tem acesso total a leitura e escrita e publica diretamente.
