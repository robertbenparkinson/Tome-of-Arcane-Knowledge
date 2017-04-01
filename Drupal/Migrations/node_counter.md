#node_counter migration 

```yml

  nid:
  totalcount:
  daycount:
  timestamp:
```

I might need to cheat and put them directly into the node_counter table

```php

db_query('INSERT INTO {node_counter} VALUES ("'.$node->nid.'", "'.$node->totalcount.'", "'.$node->daycount.'", "'.$node->timestamp.'")'); 

```
