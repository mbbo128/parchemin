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

### Create document inside test indexe
curl -XPUT 'localhost:9200/test/blabla/1' -d '{ "name": "blablabla", "author": "me"}'

### Update document
curl -XPUT 'localhost:9200/test/blabla/1' -d '{ "name": "blablabla", "author": "me", "tags": ["tagOne", "tagTwo", "tagThree"], "content": "PUT request"}'

### Test a analyzer
curl -XGET 'localhost:9200/test/_analyze?analyzer=whitespace&text=Once%20Upon%20a%20Time%20in%20America&pretty'

### Close indexe
curl -XPOST "localhost:9200/test/_close"

### Open indexe
curl -XPOST "localhost:9200/test/_open"

### Delete all indexes
curl -XDELETE 'localhost:9200/*'

### Delete all blabla indexes
curl -XDELETE 'localhost:9200/blabla*'

### Get blabla document
curl -XGET 'localhost:9200/test/blabla/1?pretty'

### Get part of a document
curl -XGET 'localhost:9200/test/blabla/1?pretty=1'_source=name,author

## Mapping

### All the types
curl -XGET "localhost:9200/index_name/_mapping?pretty"

### One type
curl -XGET "localhost:9200/index_name/type_name/_mapping?pretty"

### Update

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

### Update with file

```
curl -XPUT "localhost:9200/index_name/_settings" -d@path/setting.json
curl -XPUT "localhost:9200/index_name/index_type/_mapping" -d@path/mapping.json
```

## Query 
### Match All
```
curl -XGET 'localhost:9200/test/_search?pretty' -d '{"query": { "match_all": {}}}'
http://localhost:9200/test/_search?pretty

```
### Match 
```
curl -XGET 'localhost:9200/test/_search?pretty' -d '{"query": {"match": {"author": "me"}}}'
http://localhost:9200/test/_search?pretty&q=author:me

```
### Multi match
```
curl -XGET 'localhost:9200/test/_search?pretty' -d '{
        "query": {
                "multi_match": {
                        "query": "PUT request",
                        "fields" : ["content", "author"]
                }
        }
}'
```

### Query String
```
curl -XGET 'localhost:9200/test/_search?pretty' -d '{
        "query": {
                "query_string":{
                        "default_field": "content",
                        "query": "content:PUT^2 +content:request -content:lalala"
                }
        }
}'
```
