## Working with Content Fragments &amp; Headless Delivery (Entrega Estruturada)

- **Estrutura Neutra de Canal**: Os _Content Fragments_ (CFs) contêm conteúdo editorial estruturado e neutro, baseado em um _Content Fragment Model_

- **Canais de Entrega & Formados (HTML VS. JSON)**:
  - **HTML/Web**: O autor arrasta um componente CF para a página no AEM Sites.
  - **Headless(JSON/APIs)**: Exportação via Sling Model Exporter, REST OpenAPI ou GraphQL API.

- **In-Between Content**:
  - Permite inserir componentes e mídias no meio dos parágrafos do fragmento diretamente no Page Editor.
  - _Atenção de Prova:_ O conteúdo intermediário é salvo **na página**, e não no fragmento de origem no DAM. Se a estrutura do modelo mudar, o posicionamento do conteúdo intermediário pode sofrer desalinhamentos.

- **Reuso com MSM (Multi Site Manager)**: Quando gerenciados no console do Assets, os Content Fragments suportam MSM e Live Copies, permitindo herança e sincronização de variações e campos específicos.
