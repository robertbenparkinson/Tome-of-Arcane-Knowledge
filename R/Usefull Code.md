# Usefull Code


**Empty Data.Frame**

```R
df <- data.frame( id = integer(),
                  number = integer(),
                  name = character(),
                  stringsAsFactors = FALSE)
```


**retrieve a whole table from a MySQL DB using RMySQL

```R
library(RMySQL)
con <- dbConnect(MySQL(),
                 user="xxx", 
                 password="xxx",
                 dbname="dbxxx", 
                 host="localhost",
                 client.flag=CLIENT_MULTI_STATEMENTS)

rs <- dbSendQuery(con, "SELECT * FROM xxx_table")
dx <- dbFetch(rs, n = -1)

dx

dbDisconnect(con)
```
