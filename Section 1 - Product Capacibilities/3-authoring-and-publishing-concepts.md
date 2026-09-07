## Authoring and Publishing Concepts

O ambiente de autoria da camada de autoria oferece uma interface gráfica de usuário fácil de usar para a criação de conteúdo. Ele exige que o autor faça login utilizando uma conta à qual tenham sido atribuídos os direitos de acesso apropriados.

O AEM as a Cloud Service organiza a experiência do autor e a entrega final aos visitantes em três níveis primários

### 1. **Author Tier**

- **O que acontece aqui**: Ambiente de trabalho onde os autores produzem conteúdo utilizando uma interface gráfica amigável.
- **Ações Comuns**: Criar ou editar conteúdo nas paginas,, usar templates predefinidos, gerenciar ativos digitais, organizar estrutura do site.

### 2. **Preview Tier**

- **O que acontece aqui**: Permite que os autores e desenvolvedores testem e visualizem a experiência final exata do site antes de tornar pública.

### 3. **Publish Tier**

- **O que acontece aqui**: O local final onde o conteúdo pronto e revisado e entregue ao publico-alvo, respeitando visual e design dos templates estruturados.

### O Papel Crítico do Dispatcher

Para garantir rapidez e segurança, o **Dispatcher** e introduzido na arquitetura realizando duas funções fundamentais, **Load Balancing** e **Caching**.

- Loading Balancing: Distribui as requisições dos visitantes para evitar sobrecarga nos servidores.
- Caching: Salva copias estáticas das paginas para que nao precisem ser processadas a cada novo acesso.
