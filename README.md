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

### Match Phrase - Slop
 - Flexibiliza o match_phrase
 - Quantidade de termos que serão desconsiderados no meio de uma frase

### Wildcard
 - Retorna documentos através de wildcard patterns
   - ? – qualquer caractere uma vez
   - * zero ou mais caracteres
 - Não considera relevância
 - Evitar uso devido ao alto custo

### Fuzzy
 - Retorna documentos mesmo com termos informados incorretamente (ex: erro de digitação)
 - E distância tolerada é de 1 caractere, podendo ser
   - Alterando um caractere: box -> fox
   - Removendo um caractere: black -> lack
   - Inserindo um caractere: sic -> sick
   - Transposição entre dois caracteres adjacentes: act -> cat
 - Mesmo informando “primero”, a consulta retorna o documento com o título “Meu primeiro post”

### Nested Query
 - Permite quearrays de objetos sejam indexados de forma que cada elemento do array possa ser pesquisado de forma independente

### Quando utilizar o Elastic Stack
 - Consultas de texto que exijam alta velocidade
 - Relevância de resultados
 - Observabilidade
 - Geolocalização
 - Gerenciamento de logs
 - Cruzamento de dados e BI
 - Redução dos acessos ao banco transacional
 - Trabalhar com CQRS

### Quando não utilizar o Elastic Stack
 - Ambientes comalta escrita de dados
 - Operações transacionais
 - Fonte primária de armazenamento

### Observabilidade - Elastic APM
 - Monitora ocomportamento de todas aplicações de forma transparente
 - Monitora os acessos externos das sua aplicação (SQL, Redis, Elasticsearch, APIs de terceiros)
 - Criação de alertas com base em métricas
 - Visão da performance e inspeção e soluções de erros
 - Tomada de decisão de negócio
 - Análise e inspeção de vulnerabilidades
 - Auditoria de acessos
 - Tempo de latência de cada rota
 - Redução de custos

### Elastic APM
 - Log– Registro textual de eventos que ocorrem no sistema (Elastic Stack,Loki, GreyLog)
 - Métrica– Representação numérica baseado em uma linha do tempo (ElasticStack , New Relic, Data Dog)
 - Trace– Rastreamento de todo fluxo de uma requisição, correlação entre as requisições (Elastic Stack, Jaeger, Grafana)

### DEMO
 - Package NEST do NET para o Elastic
 - Package Serilog para colegar os logs
