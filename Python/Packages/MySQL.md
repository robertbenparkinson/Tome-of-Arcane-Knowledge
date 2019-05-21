# MySQL Python Package

## Import Statement

```python
import mysql.connector
```

## MySQL SELECT Example

```python

config = {
    'host': 'localhost',
    'user': 'name',
    'passwd': 'password',
    'database': 'example_db'
}

sql = "SELECT * FROM example_table"

mydb = mysql.connector.connect(**config)
mycursor = mydb.cursor()
mycursor.execute(sql)
myresults = mycursor.fetchall()
mydb.close()

for i in myresults:
    print(i)
```

## MySQL Examples using Python

```python
sql = "SELECT * FROM example_table"
sql = "SELECT * FROM example_table WHERE id = {}".format(id)
sql = "INSERT INTO example_table (id, url) VALUES ('{}', '{}')".format(id, url)

```