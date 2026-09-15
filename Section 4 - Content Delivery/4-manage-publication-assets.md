## Manage Publication in Assets (Publicação no DAM)

- **Destinos de Publicação no DAM**:
  - **AEM Assets (Publish)**: Destino padrão de publicação.
  - **Dynamic Media**: Publica ativos para o servidor do Dynamic Media (depende das propriedades de pastas _Selective Publish_, _Immediate_, _Upon Activation_).
  - **Brand Portal**: Exporta ativos, pastas e coleções para parceiros externos.

- **Níveis de Permissões de Publicação**:
  - **Contributor**: Pode fazer upload, mas o botão _Manage Publication_ fica oculto.
  - **Workflow User**: Pode visualizar _Manage Publication_, mas não publica diretamente; ele clica em **Request Publication** para solicitar a aprovação de um admin.
  - **Admin**: Publica diretamente ou agenda o envio futuro (_Publish Later_).

- **Filtros de Pastas**:
  - _Include folder contents (Desativado):_: Publica apenas a pasta em estado **vazio**.
  - _Include folder contents + Include only immediate folder contents (Ativados):_: Publica os ativos da pasta principal e cria as subpastas em estado vazio no Publish.
