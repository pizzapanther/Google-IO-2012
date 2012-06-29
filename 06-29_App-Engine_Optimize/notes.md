# Optimizing App Engine

* Latency vs Cost
* more efficent = lower costs

## Datastore Tips
* minimize calls
* optimize frequently viewed pages
* Use get by ID/Key not fetch(1)
* use as many gets as possible
* don't use fetch at all, call run directly
* Use projection queries, SELECT statement
* Use cursors instead of offset limie
* embedded entities
* don't index everything

## Caching
* Memcache
* Instance Caching, storing global variables
* but really use NDB instead of Instance Caching
* edge caching, cache control headers

## Batch API Requests
* operate on more than one piece of data
* Supported on: memcache, datastore, task queue, full text

## Asynchrous WOrkflow

## MOve Work Offline
* task queues

## Performance Settings
* tweak settings for lower latency or lower cost
* latency: min_idle_instances, max_pending_latency
* page speed service, static content speed
* cost: max_idl_instances, min_pending_latency
* don't use low latency and low cost together

## App Engine Servers
* different servers can have different performance settings.
