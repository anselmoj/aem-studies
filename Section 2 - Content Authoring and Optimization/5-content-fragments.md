## Content Fragments

Ativos editoriais independentes que preparam o conteúdo estruturado e neutro de canal para entrega headless.

- **Content Fragment Model**:
  - Obrigatório para criação de qualquer fragmento
  - Funciona como o esqueleto que define os campos disponíveis (títulos, booleanos, tags, referências), e os autores não podem alterar essa estrutura durante o preenchimento.

- **Associated Content**: Permite associar coleções de mídias (DAM Collections) ao fragmento, facilitando o acesso a imagens complementares aprovadas para o autor que está montando a página.

- **In-Between Content**:
  - Ao arrastar um fragmento para o editor de páginas do Sites, surge o espaço "Drag components here" entre os parágrafos do fragmento.
  - Isso permite injetar componentes extras (ex: uma imagem no meio de uma matéria de blog) diretamente na página, sem alterar o fragmento original no DAM.
  - _Atenção a prova_: O conteúdo intermediário é salvo como dado da página, e não no fragmento de origem do DAM. Se o modelo do fragmento sofrer alterações de estrutura posteriormente, o posicionamento desse conteúdo intermediário pode apresentar comportamentos inesperados.

- **REST OpenAPI vs. GraphQL para Entrega Headless**:
  - **REST OpenAPI**: Baseado em caminhos diretos para endpoints. Excelente para cache em CDNs de forma nativa (requisições GET), simplicidade de desenvolvimento e implementação de segurança simplificada.
  - **GraphQL API**: Baseado em esquemas de dados. O aplicativo solicita apenas os campos necessários, evitando payload excessivo (over-delivery). O cache de requisições POST exige a criação de _Persisted Queries_ no servidor do AEM.

- **Limites de Performance de Modelagem**:
  - **Nesting**: Mantenha o aninhamento de fragmentos na performance de busca e renderização do GraphQL.
  - **Campos Rich Text**: Evite ter mais de 10 campos Rich Text por modelo.
  - **Variações**: Recomenda-se nao passar de 10 variações por fragmento.
  - **Numero de Modelos**: Uma boa estratégia deve ter no máximo algumas dezenas de modelos (baixo "tens"). Se aproximar ou passar de 100 modelos, a estratégia de modelagem deve ser reavaliada.
