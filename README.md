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
 -  Bancodedadosnãorelacional e orientado a documentos (JSON)
 -  Armazena /busca/analisa grandes volumes quase que em tempo real
 -  Denovo:Éextremamente rápido
 -  Escalável horizontalmente[
 -   APIRest
 
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
 -  Caso não seja informado um ID, o elasticsearch fica responsável pela geração
