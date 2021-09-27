# Jaeger

jaeger is a distributed tracing system, developed by Uber
jaeger implements opentracing specification
<https://opentracing.io/specification/>
there are other tracers like, zipkin

supports many storage backends - elasticsearch, kafka, in-memory

trace -> a directed acyclic graph (DAG) of spans

tracer interface creates a span

spans contains contextual information to combine them to a trace. span
is a logical unit of work.

tags are used to add searchable key-value pairs

baggage items are added to spans, which propogate along the trace

logs can be added to traces

traces can be propogated through http headers


## architecture

* jaeger client sends spans to collector agent through jaeger agent
* collector saves the traces in db
* jaeger ui queries the db to visualize on ui
* jaeger clint implements opentracing api

## using client

* initialze global tracer
* create span from http request
* create context with span
* pass context around and create new spans wherever needed
* inject span info into new http request (adds headers)
* defer finish span
* add tags and logs wherever needed

<https://logz.io/blog/go-instrumentation-distributed-tracing-jaeger/>
