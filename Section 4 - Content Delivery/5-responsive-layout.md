## Responsive Layout, Layout Container &amp; Layout Mode (Responsividade)

- **Layout Container** (`responsivegrid`):
  - Componente container baseado em um grid responsivo padrão de **12 colunas** (`/libs/wcm/foundation/components/responsivegrid`)

- **Layout Mode & Emulator**:
  - **Layout Mode**: Recursos de interface no AEM Page Editor que permitem ao autor testar e ajustar o comportamento responsivo diretamente no ambiente de autoria.
  - Permite: redimensionar componentes no grid (_horizontal snap_), reordenar componentes e **ocultar componentes em breakpoints específicos** (ex: ocultar um banner no celular).

- **Breakpoints**:
  - Pontos de quebra definidos no modelo (_Editable Template_) ou na página raiz (ex: Phone = max 768px, Tablet = max 1200px).

- **Regra de Ouro de Aninhamento de Grid**:
  - Evite aninhar múltiplos Layout Containers. Se for inevitável, o número de colunas do container interno nunca deve ser maior do que o do container externo.
