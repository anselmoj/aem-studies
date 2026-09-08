## Experience Fragments

Agrupamentos de componentes que carregam **tanto o conteúdo quanto o layout (visual e design)**.

- **Quando usar**: Quando você precisa reutilizar uma experiência de página completa (como banners de ofertas, rodapés ou cabeçalhos baseados em modelos editáveis) em múltiplos locais ou canais externos (SaaS/Headless) sem precisar fazer "copiar e colar".

- **Experience Fragments vs. Content Fragments**:
  - **Experience Fragments**: Possuem layout e design visual. Sao compostos por componentes arrastados para um sistema de parágrafos.
  - **Content Fragments**: São puramente editoriais. Contêm apenas dados estruturados estruturados (textos, números, datas), livres de layout, cores ou fontes.
  - _Regra de Ouro_: Um Experience Fragment pode conter um Content Fragment dentro dele, mas um Content Fragment **nunca** pode conter um Experience Fragment.

- **Permissões de Escrita**: Para criar ou editar um XF, o usuário precisa necessariamente pertencer ao grupo de segurança `experience-fragments-editors`.
