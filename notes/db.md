# Databases

## Relational dbs

organized and structured

* acid
  - atomicity - each transaction succeed or fail completely
  - consistency - valid state at all times
  - isolation - no concurrency issues with multiple transactions
  - durability - persist data
* tables and columns to store data
* indexes for fast retrieval (B+ tree structure)
* DDL and DML
* Primary key, foreign key
* joins
* mysql, oracle, postgresql


mysql
* free with paid support
* mysqldump to take backup
* mysql command to restore backup
* replication
  - async, semi sync or delayed
  - read scaling - dedicate primary to writes
  - backups using replicas
  - disaster recovery
  - events in the binlog is used to replicate


## Nosql

no rigid schema. joins are hard

* document db
  - stores json like
  - mongodb
* key value db
  - redis
  - dynamodb
* wide column stores
  - store in rows with flexible columns
  - can be considered as two dimensional key value store
* graph dbs
  - nodes and edges


advantages
* flexible schemas
* scalable
* fast queries
* productivity
* less complex queries

cap theorm. we can choose only 2 out of th3 3
* consistency
* availability
* partition tolerance


* memory cache - take load off from db - memcached or couchbase
* sharding
* consistent hashing - hash independent of number of servers

## Big data

* hadoop
* map reduce
* spark - cluster computing
