## User Administration and Security

- **Grupos Nativos (OOTB)**: Possuem IDs fixos e bem conhecidos, como `administrators`, `content-authors`, `dam-users`, e `workflow-users`.

- **Grupos Sincronizados via IMS**: Criados automaticamente a partir do Admin Console e possuem a propriedade `rep:externalId` terminando em `;ims`. Servem apenas como porta de entrada e nao devem receber ACLs diretas.

- **Content Hub e Brand Portal**:
  - O acesso ao Content Hub é concedido estritamente pelo perfil **Limited User** (o perfil _Power User_ sozinho não dá acesso ao Content Hub).
  - Alterações efetuadas no Admin Console levam entre 5 a 10 horas para sincronizar com o Brand Portal devido a um job em background que roda a cada 8 horas.
