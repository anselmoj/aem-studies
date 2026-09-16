## Creating and Synchronizing Live Copies

- **Blueprint Configurations**: Definem a estrutura de origem (página raiz, ramos de idioma e capítulos/subpáginas) usada para gerar Live Copies.

- **Sincronização**: Permite selecionar o escopo do _Rollout_ (página e subpáginas), agendar disparos e controlar a herança (cancelar herança em componentes específicos ou redefinir via _Reset_).

- **Deep vs. Shallow Live Copies:**
  - _Deep Live Copy:_ Herda a página selecionada e toda a sua árvore de subpáginas.
  - _Shallow Live Copy:_ Herda **apenas** a página raiz selecionada (não herda subpáginas).

- **Acoes de Governança de Herança**:
  - **Cancel Inheritance**: Quebra temporariamente a herança em um componente ou propriedade para permitir customização local.
  - **Re-enable / Revert Inheritance:** Reativa a herança com a origem.
  - **Reset:** Cancela todas as alterações locais e restaura o estado exato do Blueprint.
  - **Suspend:** Pausa o recebimento de atualizações de rollout.
  - **Detach:** Remove permanentemente o vínculo entre a Live Copy e o Blueprint (não reversível).
