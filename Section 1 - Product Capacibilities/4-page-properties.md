## Page Properties

As propriedades da página podem controlar diversos aspectos de uma página, desde um titulo e a identidade visual ate as permissões.
Essas propriedades estão distribuídas em varias tabs, algumas das quais podem estar ocultas, dependendo do tipo de página. Assim como a maioria das propriedades do AEM, as propriedades da página podem ser herdadas.

### Aba Básica (Basic Tab)

- **Title**: E um campo **obrigatório** usado para fins de SEO e exibido em vários locais da interface, como os consoles de visualização (cards e listas) no Sites Console
- **Navigation Title vs. Page Title**: Se o autor deseja um titulo mais curto ou conciso no menu de navegação, ele especifica o **Navigation Title**. Se este campo estiver vazio, o sistema usara o **Page Title** por padrão.
- **Branding**: Permite anexar um sufixo da marca ao titulo da página (ex: Cycling Tuscany | Always ready for the WKND).
- **On/Off Time (Agendamento de exibição)**:
  - Configurar um On Time ou Off Time **não altera o status de publicação da página**. O Conteúdo continua exibindo fisicamente na instancia Publish, mas fica em estado "dormente" para os visitantes ate a data estipulada.
  - Como essa configuração lida estritamente com conteúdos que ja foram publicados, **os fluxos de trabalho (workflows) de aprovação não sao disparados** pelas datas de On/Off Time.
- **Vanity URL**: Devem ser únicas, **não suportam expressões regulares (regex) e não devem ser associadas a uma pagina que ja existe**.

### Aba Avançada (Advanced Tab)

- **Language Root**: Deve ser marcada se a página em questão for o ponto de partida (raiz) de uma **copia de idioma (Language Copy)**.
- **Alias**: Cria a propriedade sling:alias no nó da página no repositório. -**Template Settings (Allowed Templates)**: Limita quais modelos de página podem ser usados na criação de subpáginas a partir daquele ramo
  . Cada entrada deve conter um caminho absoluto e o uso de /.\* permite liberar todos os templates abaixo daquela pasta.
- **Authentication Requirement**:
  - Permite restringir o acesso à página exigindo login.
  - A página de login especifica deve ser publica e nao pode exigir autenticação.
