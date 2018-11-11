# Elasticsearch

## Installation

### Plugin Sense Chrome
http://teknosrc.com/chrome-elasticsearch-sense-ui-plugin-not-working-solved-solution/

### Install plugin head
- https://github.com/mobz/elasticsearch-head

### Check installed plugin head
2 options
- http://localhost:9200/_nodes/plugins?head
- curl -XGET "localhost:9200/_nodes/plugins?head"

### Access installed plugin head
http://localhost:9200/_plugin/head/

## Indexe

### Create test indexe
curl -XPUT "localhost:9200/test" 

### Close indexe
curl -XPOST "localhost:9200/test/_close"

### Open indexe
curl -XPOST "localhost:9200/test/_open"

## Mapping

### all the types
curl -XGET "localhost:9200/index_name/_mapping?pretty"

### one type
curl -XGET "localhost:9200/index_name/type_name/_mapping?pretty"

### update

```
curl -XPUT "localhost:9200/index_name/index_type/_mapping" -d '{
  "properties" : {
    "new_field_name": {
      "type": "integer"
    }
  }
}'
```
The mapping definition of an existing field cannot be changed
