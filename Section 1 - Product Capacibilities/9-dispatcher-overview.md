## Dispatcher Overview

O Dispatcher é a ferramenta oficial de armazenamento em cache e balanceamento de carga da Adobe usada em conjunto com servidores web corporativos (como Apache ou IIS)

### 1. Onde ele atua? (Publish vs. Author)

- **Caso Comum (Publish)**: O uso mais comum do Dispatcher é armazenar em cache as respostas vindas de uma instância de **AEM Publish**, blindando o servidor contra sobrecarga de requisições e aumentando drasticamente a segurança e a velocidade de resposta para os visitantes do site
  .
- **Caso Especial (Author)**: O documento traz um detalhe crucial para cenários de prova: o Dispatcher **também pode ser usado para aumentar a velocidade de resposta da instância de Author** . Isso é altamente recomendado se você tiver uma equipe muito grande de autores editando e atualizando o site de forma simultânea.

### 2. Os Dois Métodos de Atualização de Cache

Quando um autor ativa (publica) um conteúdo no AEM, o Dispatcher tem duas formas de garantir que o cache não fique obsoleto:

- **Content Updates (Atualizações de Conteúdo)**: O AEM envia uma requisição para o Dispatcher para remover fisicamente os arquivos modificados do cache do sistema
  . Ele deleta o arquivo alterado e todos os outros que começam com o mesmo padrão (ex: se /en/index.html mudar, todos os arquivos que começam com /en/index. são excluídos)
  . Além disso, ele toca no arquivo statfile para atualizar o seu carimbo de data/hora (timestamp)
  .
- **Auto-Invalidation (Auto-invalidação)**: Ideal para arquivos com relações complexas (como páginas HTML cheias de links e menus de navegação)
  . Esse método não deleta fisicamente nenhum arquivo no momento da publicação
  . Ele apenas atualiza o timestamp do statfile
  . Quando o visitante solicita uma página que está na lista de auto-invalidação, o Dispatcher compara a data do arquivo em cache com a do statfile: se o arquivo em cache for mais antigo, ele busca a versão nova e atualizada diretamente no AEM
  .

### 3. O que o Dispatcher NÃO armazena em cache por padrão?

A Adobe adora cobrar as exceções de cache. O Dispatcher sempre ignora o cache e faz a requisição diretamente ao AEM nos seguintes casos:

- Se a URI da requisição contiver um ponto de interrogação ? (o que geralmente indica páginas dinâmicas, como uma página de busca com parâmetros).
- Se o arquivo não possuir extensão (pois o servidor web necessita da extensão para identificar o tipo de mídia ou MIME-type).
- Se o cabeçalho de autenticação (Authentication Header) estiver ativo e configurado para barrar o cache.
- Nota: Apenas requisições que utilizam os métodos HTTP GET ou HEAD são qualificadas para cache por padrão.

### 4. Load Balancing & Sticky Connections (Conexões Persistentes)

- **Load Balancing**: Distribui a carga computacional das visitas entre várias instâncias de Publish do AEM, garantindo maior processamento e resiliência contra falhas (se uma instância cair, o Dispatcher redireciona o tráfego de forma invisível para as outras).
- **Sticky Connections**: Se o seu site possui páginas personalizadas ou dados de sessão do usuário, as requisições desse visitante devem retornar estritamente para a mesma instância do AEM onde a sessão foi iniciada
  . O Dispatcher gerencia isso via Sticky Connections
  . Contudo, para páginas com conexões persistentes, o cache geralmente deve ser desativado para evitar que um usuário acabe visualizando os dados de sessão de outro
  .
