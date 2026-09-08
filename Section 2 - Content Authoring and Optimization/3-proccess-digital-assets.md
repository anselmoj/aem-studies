## Process Digital Assets

Como o AEM processa mídias e garante a automação de conformidade de marca.

- **Workflow "DAM Update Assets"**:
  - Por padrão, todos os ativos que sofrerem uploads no AEM sao processados automaticamente por esse fluxo.
  - Ele realiza tarefas fundamentais de sanidade de ativos: gera rendições, faz a extração e writeback de metadados, e executa mídias e tags inteligentes (Smart Tags) com o motor de inteligência artificial do **Adobe Sensei**.

- **Workflow Launcher**:
  - Administradores podem configurar launchers que monitoram modificações no repositório e disparam fluxos automáticos com base em condições predefinidas (ex: aplicar marca d'água em fotos que entram na pasta `/photos/freelancers/`).

- **Boas Práticas de Renditions**:
  - Rendições geradas que não serão utilizadas no futuro ocupam **muito espaço de armazenamento** e não podem ser apagadas em lote pela interface. Remova essas etapas inúteis de geração diretamente do workflow antes de rodar o DAM.
  - No entanto, **nunca remova as rendições de miniaturas (thumbnails) e web renditions padrão** do workflow "DAM Update Asset", ou a interface do AEM Assets falhará em renderizar o painel e os previews das imagens.
