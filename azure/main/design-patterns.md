### Data Management
* `Cache-Aside` - load data on demand into a cache from a data store
    * Reading form cache is fast, but it may expire
* `CQRS` - separate read and update operations 
* `Event Sourcing` - add actions to event store -> which notifies consumers -> who apply changes in DB
* `Index Table` - create indexes for frequently accessed fields
* `Materialized View` - generate prepopulated views
* `Sharding` - each shard has same schema but different data
* `Static Content Hosting` - static content to a cloud-based storage service (e.g. CDN)
* `Valet Key` - token which gives access to specific resource

### Design and Implementation
* `Ambassador` - client-side proxy (retry, circuit breaking, monitoring, security)
* `Anti-Corruption Layer` - adapter between modern and legacy application
* `Backends for Frontends` - different backend for each frontend (e.g. for desktop/mobile)
* `Compute Resource Consolidation` - combine tasks into single unit
* `External Configuration Store` - move config to centralized location
* `Gateway Aggregation` - use gateway to combine multiple requests into a single one
* `Gateway Offloading` - move shared functionality to a gateway (e.g. traffic decryption)
* `Gateway Routing` - route requests to multiple services (via gateway)
* `Leader Election` - elect one instance as leader (to manage other instances)
* `Pipes and Filters` - break complex processing to simple parts
* `Sidecar` - move part of app to different container (for isolation and encapsulation)
* `Strangler Fig` - incrementally modernize legacy system by replacing its parts with new services

### Messaging


[Source](https://docs.microsoft.com/en-us/azure/architecture/patterns/index-patterns)
