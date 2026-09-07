## Integration with Adobe Target

O Adobe Target é a ferramenta do ecossistema Experience Cloud responsável por aumentar a relevância do conteúdo por meio de testes e personalização em todos os canais.

### 1. Requisitos para a Integração Funcionar

- **1 Configuração no AEM via Touch UI**: Criar uma configuração do Target dentro do AEM, que exige uma integração com o Adobe IMS
- **Configuração no Adobe Launch**: O Launch é obrigatório para gerenciar as propriedades client-side (tags e bibliotecas Javascript, como a at.js) nas páginas do AEM
  . Sem o Launch, as bibliotecas do Target não são renderizadas e o "Experience Targeting" não acontece

### 2. Exportação de Fragmentos (Experience e Content Fragment)

- Se o seu objetivo de negócio for exportar **Experience Fragments** ou **Content Fragments** do AEM diretamente para o Adobe Target (para serem usados como ofertas personalizadas por lá), você precisa ter a Configuração do Adobe Target e a Integração IMS ativas no AEM.

### 3. A Diferença de Negócio: Target Standard vs. Premium

Durante a configuração, os perfis de produto exibidos dependem do seu licenciamento.

- **Adobe Target Standard**: Apenas o workspace padrão fica disponível listado para escolha.
- **Adobe Target Premium**: Todos os workspaces configurados na sua organização são listados para escolha.

### 4. Tenant ID vs. Client Code

Na maioria dos clientes, o Tenant ID e o Client Code são idênticos
. No entanto, o AEM os diferencia da seguinte forma:

- **Tenant ID**: É a chave utilizada para todas as chamadas de **back-end** (envia para o servidor) para o Target.
- **Client Code**: É a chave utilizada para as chamadas **client-side** (executadas diretamente no navegador do visitante)

### 5. Mudança de Arquitetura (Classic UI vs. Touch UI)

A Adobe adora cobrar a mudança de caminhos do repositório JCR entre as versões clássicas e modernas
:
Classic UI (Antigo): As configurações de nuvem ficavam salvas em `/etc/cloudservices/testandtarget/` e permitiam múltiplas configurações soltas
.
Touch UI (Cloud Service / Moderno): A configuração única fica sob o tenant em `/conf/tenant/settings/cloudconfigs/target/`
