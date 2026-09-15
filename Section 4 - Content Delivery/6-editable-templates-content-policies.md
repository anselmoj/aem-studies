## Editable Templates &amp; Content Policies (Modelos Editáveis)

- **Três Elementos do Editable Template**
  1.  **Structure**: Componentes fixos definidos pelo autor do template (bloqueados) que aparecem em todas as páginas e não podem ser alterados pelo autor da página.
  2.  **Initial Content**: Componentes pré-preenchidos que surgem na criação da página, mas que o autor da página pode editar ou deletar.
  3.  **Content Policies**: Definem quais componentes são permitidos dentro de cada container e quais estilos do _Style System_ estão disponíveis.

- **Propriedade `cq:allowedTemplate`** :
  - Definida nas _Page Properties_ da página raiz para controlar quais modelos editáveis estão disponíveis nas subpáginas.

- **Grupos de Acessos**:
  - Para criar/editar templates editáveis, o usuário deve obrigatoriamente pertencer ao grupo **`template-authors`**.
