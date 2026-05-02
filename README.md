Curso Treinamento ElasticStack no nextwave(LuisDEV)

### Porque utilizar o Elastic Cloud ?
 - “Tenha confiança e segurança ao obter dados de qualquer fonte, em qualquer formato, para buscar, analisar e visualizar tudo em tempo real”
 - “Onde tiver dados, você pode usar o Elastic”

 ### Elastic Stack ?
  - Elasticsearch: Mecanismo de pesquisa RESTful distribuído responsável pelo armazenamento de documentos (JSON) com Especialidade em busca Fulltext(Muito rápido)
  - Logstash: Componente de processamento de dados do Elastic Stack que recebe, transforma e envia dados para o Elasticsearch
  - Kibana: Interface web para pesquisa, criação e visualização de gráficos/dashboards (Canvas) e configuração de alertas.
  - Beats: Agentes de coletas de dados de propósito único que podem enviar informações de centenas ou milhares de máquinas para o Logstash ou para o Elasticsearch.

### Elasticsearch
 - Banco dedados não relacional e orientado a documentos (JSON)
 - Armazena /busca/analisa grandes volumes quase que em tempo real
 - Denovo: É extremamente rápido
 - Escalável horizontalmente[
 - APIRest
 
### Queries no Elasticsearch
 - Querystring
   - Podeserusado diretamente na URL
   - Simples efácil de usar
   - Difícil de escrever queries complexas
 - QueryDSL(domain specific language)
   - Query enviada no corpo darequisição REST
   - Expõe toda acoleção deAPIs do elasticsearch
   - Poderoso

### Criando um documento - POST
 - Também pode ser utilizado o POST (método de atualização)
 - Caso não seja informado um ID, o elasticsearch fica responsável pela geração
 
 ### Atualizando documentos
 - O JSON enviado no POST substituirá o documento existente no índice
 - No exemplo abaixo, os campos titulo e categoria seriam modificados e o campo autor seria excluído do documento

### Atualização parcial de documentos
 - Utilizar a API _update, conforme exemplo abaixo

### Exclusão de documentos
 - DELETEblogs/_doc/1
 - Se DELETE blogs for executado sem passar type e id, o índice inteiro éexcluído    

### Tipos de queries no Elasticsearch
 - Match
 - MatchPhrase
 - MatchPhrase Prefix
 - Wildcard
 - Range
 - Fuzzy
 - Nested
 - Combinando Queries
 - Paginação
 - Highlight
 - Aggregations

### Match Query com SHOULD MATCH
 -  Informa a quantidade mínima de termos que necessitam dar match para retornar o documento

### Match Phrase
 - Todos os termos devem dar match na ordem
 - A frase é consideradaa partir do primeiro termo encontrado

 
