## Integration With Adobe Analytics

A integração com o Adobe Analytics permite rastrear e analisar a atividade das páginas do seu site
. No AEM as a Cloud Service, essa arquitetura foi modernizada e simplificada, removendo ferramentas legadas e transferindo a inteligência técnica para a ponta.

### A Grande Mudanca de Arquitetura

- **Fim dos Frameworks no AEM**: Ao contrario das versões anteriores do AEM, o suporte a frameworks de mapeamento nao e mais fornecido na configuração do Analytics no AEM as A Cloud Service.
- **Adobe Launch como Unica Fonte de Verdade**: Todo o mapeamento de variáveis (eVars, props, eventos) e a injeção das bibliotecas Javascript agora ocorrem **exclusivamente dentro do Adobe Launch**. O Launch substituiu completamente o modelo antigo gerenciado pelo Sitecatalyst.

### Analytics vs. CJA vs. Target

Quando devemos indicar cada uma das soluções em cenários de negócio:

- Se o cliente precisa **rastrear o comportamento web tradicional**(cliques, visualizações de pagina, conversões de formulários): **Adobe Analytics**
- Se o cliente precisa **reunir jornadas de dados complexas, cruzando dados online com sistemas físicos** (ex: Call Center, compras em Lojas Físicas / POS): **Customer Journey Analytics (CJA)**.
- Se o cliente precisa **entregar experiências dinâmicas, testes A/B ou ofertas personalizadas** com base nesses perfis: **Adobe Target**.
