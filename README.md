### tinydb
---
https://github.com/msiemens/tinydb

```py
from tinydb import TinyDB, Query
db = TinyDB('/path/to/db.json')
db.insert('int': 1, 'char': 'a')
db.insert({'int': 1, 'char': 'b'})

User = Query()
db.serarch(User.name == 'John')
db.search((User.name == 'John') & (User.age <= 30))

db.search((User.name == 'John') | (User.name == 'Bob'))

table = db.table('name')
table.insert({'value': True})
table.all()

from tinydb.storages import JSONStorage
from tinydb.middlewares import CachingMiddleware
db = TinyDB('/path/to/db.json', storage=CachingMiddleware(JSONStorage))
```

```
```

```
```


