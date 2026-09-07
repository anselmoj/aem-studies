## AEM Screens

E uma solução digital que permite criar, publicar e exibir experiencias digitais dinâmicas e interativas. A solução envolve diversos tipos de telas de exibição no local, integradas a uma estrategia de marketing omnichannel.

### O que o AEM Screens permite criar

- Aplicações práticas: Menu boards digitais de restaurantes, recomendadores de produtos e exibição de mídias de estilo de vida em segundo plano para ambientação.
- Uso em ambiente físicos: Telas de interatividade em lojas, totens, reforço de branding e criação de atmosfera nos estabelecimentos.

### AEM Sites vs. AEM Screens

- Tempo de permanência (**Dwell-time**): Na web (AEM Sites), as páginas contem uma grande riqueza de detalhes para leitura longa e calma. No Screens(em loja), as experiências devem ser altamente direcionadas, curtas e de consumo visual rápido, antecipando as necessidades do cliente que esta de passagem.
- Distancia de Visualização (**Viewing Distance**): As telas físicas estão muito mais distantes do olho do usuário do que um monitor, por conta disso o tamanho do texto deve ser consideravelmente maior e o espaçamento deve ser testado de acordo com a dimensão física da tela e sua localização real no espaço.
- Experiencias Interativas via SPA Editor: Podemos criar aplicações de toque (para quiosques e totens) usando o AEM em conjunto com SPA Editor. Como boa pratica, devemos configurar o **Inactivity Timer** para resetar a tela de volta ao estado inicial quando o cliente for embora, além de manter as chamadas para ação claras e fáceis.
- Incompatibilidade de Componentes: **Muitos componentes nativos do AEM Sites NÃO funcionam no AEM Screens**. O AEM Screens possui uma biblioteca própria de componentes prontos para uso (out-of-the-box). Se houver necessidade extrema de colocar uma pagina do AEM Sites dentro de um canal do Screens, ele deve ser formatada, previamente para as dimensões exatas do display de destino.
