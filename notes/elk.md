# ELK stack

Elasticsearch, Logstash (and beats), Kibana

* beats -> data collection (ties with kafka, redis etc for buffering)
* logstash -> data aggregation and processing
* elasticsearch -> storage and indexing
* kibana -> analysis and visualization

beats
* file beat
* metric beat
* packet beat

elasticsearch
* indexing for fast retrieval
* rest api
* plugins


logstash
* collect and format logs
* lot of plugins
* input/filter/output plugins
* input/output codecs

kibana
* ui for elasticsearch
* create dashboards


## Production grade ELK

* save and index all log files
* operate even when prod systems are overloaded
* security
* data retention policy, upgrades etc


* use buffer in front of logstash to make sure not to lose data
* monitor logstash/elasticsearch exceptions
* scale in all fronts
* use kafka buffer and replicate kafka as well
* monitor kafka
* run logstash replicas across zones
* use elasticsearch cluster with atleast 3 master nodes
* block kibana access using reverse proxy auth
* have retention policy, archive
* log consistency (structure)
* grok plugin - convert unstructured to structured
* upgrades
* use correct mapping for fields (elasticsearch will try to auto map)
* estimate capacity
* rename clusters for production
* careful with logstash config


## Use cases

* development and troubleshooting
* cloud operations and monitoring
* APM - application performance monitoring
* security and compliance (access logging, gdpr etc)
  - anti ddos by analysis of logs
* business intelligence
* SEO
