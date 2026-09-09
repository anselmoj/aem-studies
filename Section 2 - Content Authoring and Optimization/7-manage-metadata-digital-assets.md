## Manage Metadata of your Digital Assets

A inteligencia por trás da catalogação e automação de arquivos.

- **As Três Categorias de Metadados**:
  1. **Technical**: Propriedades mecânicas (tamanho, formato, resolução, dimensões, modo de cores).
  2. **Informational**: Facilitam a busca (palavras-chave, legendas, descrições).
  3. **Administrative**: Regras de ciclo de vida e jurídicas (proprietário, direitos de uso, termos de licença, permissões).

- **Formatos e Codificação**:
  - **XMP**: O padrão aberto da Adobe que armazena todos os metadados dentro do JCR do AEM.
  - **ID3**: Usado para extrair informações de mídias de áudio (MP3).
  - **Exif**: Armazena metadados de fotografia digital, mas **possui limitação técnica de nao rodar em arquivos como BMP, GIF ou PNG**.

- **Edição em Massa (Bulk Metadata Editing)**: Ao selecionar múltiplos arquivos, o AEM exibirá apenas os campos comuns mais baixos ("lowest common parent form") compartilhados por todos os arquivos.
- **Append Mode**: Quando ativo, anexa novas tags e metadados nos campos de múltiplos valores ao invés de limpar e sobrescrever o conteúdo antigo.
