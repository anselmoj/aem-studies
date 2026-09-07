## Customer Journey Analytics

O Customer Journey Analytics (CJA) é a solução de análise de próxima geração da Adobe que leva o poder do Analysis Workspace para os dados armazenados no Adobe Experience Platform (AEP)
. Enquanto o Adobe Analytics tradicional se concentra em dados puramente web ou de aplicativos, o CJA permite visualizar o cliente em um contexto de jornada completa, sequenciando canais offline (como call centers e sistemas de Ponto de Venda - POS) e online em uma única visualização de relatório.

### Mudança de Terminologia

| Adobe Analytics Tradicional | Customer Journey Analytics (CJA) |
| --------------------------- | :------------------------------: |
| Virtual Report Suites       |            Data Views            |
| Classifications             |         Lookup Datasets          |
| Customer Attributes         |         Profile Datasets         |
| Hit Containers              |         Event Containers         |
| Visit Containers            |       Sessions Containers        |
| Visitor Containers          |        Person Containers         |

### Mecânica Técnica Base: XDM e SQL

- O CJA utiliza o modelo XDM (Experience Data Model) para representar e organizar os dados de forma uniforme antes da exploração.
- Os analistas podem usar o **Adobe Experience Platform Query Service** para executar consultas e manipulações complexas de dados usando ferramentas e frameworks compatíveis com **SQL padrão**.
