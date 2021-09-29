# Monitoring and instrumentation

Ways to monitor
* traces -> to see how control flows in a distributed system
* logs -> for debugging, analysis
* metrics -> to track performance, health status, latency etc
  * latency
  * traffic
  * errors
  * saturation -> how much more it can handle before it breaks down

  alerting -> notify relevent teams/people when things go wrong (or
  about to go wrong)
  and take some action to rectify that automatically or manually

  one of the responsibilities of an SRE include responding to alerts and
  making sure that it won't happen again

* ss command -> socket statistics
* top/ps -> processes
* df -> disk usage stats
* tcpdump -> capture network traffic


metric types
* guage
* counter
* timer

have runbook for alerts

thanos
- open source HA prometheus setup with long term storage
- adds sidecar to promethus servers
- sidecar can push data to storge backends
