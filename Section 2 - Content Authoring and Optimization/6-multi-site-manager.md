## Multi Site Manager (MSM) for Assets

Reutilização de ativos digitais de forma sincronizada e padronizada em diferentes canais.

- **Diferenças Chave entre MSM para Sites e MSM para Assets**:
  - No Sites, o arquivo de origem é chamado de **Blueprint**. No Assets, é chamado de **Live Copy Source**.
  - Bloquear propriedades de páginas e remover a etapa de capítulos nao funcionam no Assets.
  - No Assets, a única configuração de sincronização aceita e a padrão(**Standard rollout config**).

- **Ciclo de Vida de Sincronização**:
  - **Rollout**: Ação iniciada na origem que força o envio (push) das atualizações para as Live Copies.
  - **Synchronize**: Ação iniciada na Live Copy que busca (pull) as mudanças da origem. Respeita modificações locais onde a herança foi quebrada.
  - **Suspend**: Pausa a herança temporariamente. A Live Copy não é atualizada, mas a relação de parentesco continua ativa.
  - **Reset**: Desfaz qualquer alteração local feita na Live Copy e reestabelece todas as heranças, tornando-a novamente uma cópia idêntica à origem.
  - **Detach**: Quebra a relação permanentemente. O ativo vira um arquivo avulso comum e nunca mais poderá ser sincronizado.

- **Herança de Metadados Individuais**: Você pode fazer alterações pontuais em metadados específicos de um arquivo na Live Copy (ex: traduzir o título da foto apenas para a versão local) clicando em **Cancel Inheritance** ao lado do campo desejado. O restante das propriedades continuará herdando as mudanças da origem normalmente.
